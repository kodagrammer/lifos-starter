# 배포자 안내

## 공개 템플릿 게시

1. 공개할 파일은 `lifos-starter` 배포 폴더만 사용합니다. 원래 개인 시스템의 저장소·이력·상위 폴더를 복제하지 않습니다.
2. 실제 사용자 이름·연락처·계좌·개인 문서 URL·토큰·개인 설정 파일이 없는지 검토합니다. `personal/`에는 README와 `.example.md` 파일만 있어야 합니다.
3. GitHub에서 새 **Public** 저장소 `lifos-starter`를 만듭니다.
4. 검토한 배포 폴더 **안의 내용**을 저장소 루트에 올립니다. `lifos-starter/lifos-starter/README.md`처럼 한 단계 중첩하지 않습니다. 숨김 파일 `.gitignore`도 포함합니다.
5. README·프롬프트·문서 링크가 GitHub에서 열리는지 확인합니다.
6. **Settings → General → Template repository**를 켭니다.
7. 새 Private 개인 사본을 실제로 만들어 파일·공개 범위를 확인합니다.
8. 가상 연습과 비개발자 파일럿 전에는 이를 완료했다고 홍보하지 않습니다.

게시 주소는 실제 생성된 뒤 공유합니다. 이 양식에는 가짜 소유자 URL이나 생성 버튼 링크를 넣지 않았습니다. GitHub 저장소 자체의 `Use this template` 버튼을 사용합니다.

## 왜 fork 후 연결 끊기를 기본 안내로 쓰지 않는가

로컬 복사본의 원격 주소를 새 Private 저장소로 바꾸면 별도 저장소로 업로드할 수 있습니다. 하지만 로컬 주소를 바꿔도 GitHub에 이미 만든 공개 fork의 관계·공개 파일·이력은 사라지지 않습니다. `git init`도 이미 있는 Git 이력을 자동 초기화하는 절차가 아닙니다.

따라서 비개발자에게는 **Use this template → 새 Private 생성**을 기본으로 안내합니다. 새 저장소가 만들어지므로 연결 해제 작업이 필요하지 않습니다. 공개 fork에 개인 자료를 넣었다가 비공개로 전환하는 경로는 안내하지 않습니다.

## Template 기능을 쓸 수 없는 경우

배포자가 Template 설정을 켜는 것을 먼저 해결합니다. 다운로드 파일만 받은 경우에는 다음 방법으로 새 비공개 사본을 만들 수 있습니다.

1. GitHub에서 **New repository**를 눌러 `lifos-personal`을 **Private**로 생성합니다. README를 하나 만들도록 선택하면 파일 업로드 화면을 찾기 쉽습니다.
2. 받은 공개 골격 ZIP을 PC에서 풉니다.
3. 저장소에서 **Add file → Upload files**로 골격 폴더 안의 내용을 올립니다. 임시 README는 제공된 README로 교체합니다.
4. `.gitignore`를 포함한 파일 목록과 Private 표시를 확인합니다.
5. 개인 데이터는 이 단계가 끝난 뒤에만 입력합니다.

이 방법도 공개 fork를 먼저 만들지 않습니다. 기존 개인 시스템의 Git 이력을 업로드하지 않습니다.

## 라이선스와 버전

범용 골격은 MIT License로 배포합니다. 개인 금융 기록을 공개하도록 요구하지 않습니다. 원본 배포를 개선할 때 CHANGELOG와 버전을 갱신하고, 개인 사본의 운영 설정이나 데이터를 포함하지 않습니다.

공식 근거: [Template repository 설정](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository), [새 템플릿 사본 생성](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template), [별도 저장소 복제](https://docs.github.com/en/repositories/creating-and-managing-repositories/duplicating-a-repository).
