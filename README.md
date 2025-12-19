# test-project
Backlog連携のテスト中です
テストがうまくいきません


1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
name: Backlog Notify
 
on:
  push:
  pull_request:
    types:
      - opened
      - reopened
      - ready_for_review
      - closed
 
jobs:
  notify:
    runs-on: ubuntu-latest
    steps:
      - name: Backlog Notify
        uses: bicstone/backlog-notify@v5
        with:
          project_key:A1
          api_host: lwo.backlog.com
          api_key: ${{ secrets.BACKLOG_API_KEY }}
