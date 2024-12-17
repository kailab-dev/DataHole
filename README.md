# DataHole(다양한 포멧의 파일로부터 텍스트 및 이미지를 처리하기 위한 C#용 라이브러리)
- DataHole Community
이 소프트웨어와 포함된 라이브러리는 다양한 문서 포멧으로부터 텍스트와 이미지를 추출하고 활용하기 위해 만들어진 무료 소프트웨어입니다.
지속적인 개발 지원을 위해서 유료 구독을 게시글로 요청하실 수 있습니다.

# 업데이트 로그
- 2024.12.15 : 0.5버전
  - 현재 지원 포멧 : hwp, hwpx, hml(hwpml), doc, docx, pptx, xlsx, jpeg, jpg, png, pdf, txt, html
  - 크로스 플랫폼(Linux, Windows)에 대한 테스트 및 서비스 지원
  - 기타 버그 수정
- 2024.04.01 : 최초 릴리즈
  - 현재 지원 포멧 : hwp, hwpx, doc, docx, pptx, xlsx, jpeg, jpg, png, pdf, txt, html

# 사용방법
> 릴리즈에서 0.5 버전을 다운로드 후 DataHole.DocProcessing를 참조에 추가하여 사용하시면 됩니다.

```
                DocumentFilter _docFilter = new DocumentFilter();
                var _df = _docFilter.DoProcessing(new string[] { 파일명 }).ToList<DocumentFilterResult>();

                if (_df[0] != null)
                {
                    var _textList = _df[0].TextList;     // 텍스트 목록
                    foreach (string _text in _textList)
                    {
                        Console.WriteLine(_text + "\r\n");
                    }

                    var _imgList = _df[0].Images;     // 이미지 목록

                }
```
 
# 업데이트 주기
- 긴급 업데이트는 이슈에 따라 비정기적으로 진행됩니다.

# 향후 개발 내용
- 표에 대한 추출 개선(MD 포멧 또는 CSV 형태로 별도 출력 제공)
- 문서 포멧 변환기능 제공

# 의존성
- PDF 파일은 PdfPig를 통해 처리됩니다.
- 크로스플랫폼에서 이미지 처리를 위해 SkiaSharp가 이용됩니다.
- OCR은 PaddleOCR을 통해 처리합니다.

# 라이센스
- 본 소프트웨어는 개인 및 기업에서 무료로 사용이 가능한 라이브러리입니다.
- 사용된 오픈소스 라이브러리들은 개별 라이브러리들은 각각의 라이센스에 따름
- 해당 프로그램은 개인적 용도 및 상업적 용도로 무료로 이용이 가능
- 기술지원을 위해서는 별도의 라이센스를 요청할 수 있음

# 기타
- 라이브러리의 hwp계열 파일(hwp, hwpml, hwpx)에 대한 처리기는 "한글과컴퓨터"에서 오픈한 문서 포멧을 활용하여 개발되었습니다.
- 라이브러리의 doc, ppt, xls, docx, pptx, xlsx 파일 처리는 Microsoft에서 공개한 포멧 문서를 활용하여 개발되었습니다.



