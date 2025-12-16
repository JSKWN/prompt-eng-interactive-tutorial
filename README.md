# Anthropic의 프롬프트 엔지니어링 인터랙티브 튜토리얼

인공지능 모델인 **Claude**에 최적화된 프롬프트 설계 지식을 제공하는 오픈 소스 학습 자료입니다.

OpenAI 기반 챗봇 학습 플로우와 유사하지만, Claude 모델의 특장점 및 한계 인지, 그리고 실전 연습 중심의 구성 덕분에 타 튜토리얼 대비 실제 업무 적용 가능성과 실용성이 뛰어납니다. 특히 실제로 프롬프트 작성과 결과 실험을 병행할 수 있어 초보 엔지니어에게 큰 이점을 제공합니다.

## 코스 소개 및 목표

이 튜토리얼은 Claude 내에서 최적의 프롬프트를 설계하고 활용하는 법을 단계별로 안내합니다. 코스 완료 시 사용자는 아래 내용을 습득할 수 있습니다.

*   효과적인 프롬프트 구조의 이해
*   대표적인 실패 패턴 인지 및 우선 개선법 (80/20 법칙)
*   Claude 모델의 강점과 약점 파악
*   다수의 일반 업무에 적용할 프롬프트 구축 능력

## 코스 구조 및 콘텐츠

*   **구성:** 9개 장(초급 ~ 고급)과 심화 부록으로 구성되어 있음
*   **방식:** 각 장은 이론 설명과 직접 실습을 함께 제공함
*   **실습 환경:** 각 파트 마지막에는 "Example Playground"에서 프롬프트를 직접 입력하고, 응답의 변화를 실험할 수 있는 공간이 마련되어 있음
*   **해설:** 모든 예시에 대해 해설 키가 포함되어 있음
*   **모델:** 튜토리얼의 기본 모델은 가장 경량이면서 빠르고 저렴한 **Claude 3 Haiku**임 (필요시 더 높은 지능의 Sonnet 및 Opus에 대한 언급도 포함)
*   **접근성:** Google Sheets 확장 버전으로도 활용할 수 있어 학습 접근성이 높음

## 커리큘럼 목차

### 초급
*   **Chapter 1:** 기본 프롬프트 구조
*   **Chapter 2:** 명확하고 직접적인 지시 작성법
*   **Chapter 3:** 역할 부여하기

### 중급
*   **Chapter 4:** 데이터와 지시 분리
*   **Chapter 5:** 출력 포맷 지정 및 Claude를 위한 대화화
*   **Chapter 6:** 사전 사고(단계별 생각 도출)
*   **Chapter 7:** 예시 활용법

### 고급
*   **Chapter 8:** 환각(Hallucination) 방지
*   **Chapter 9:** 복잡한 프롬프트 구축(산업별 사례)
    *   *예: 챗봇, 법률 서비스, 금융 서비스, 코딩 등 다양한 업무별 실전 적용 문제를 다룸*

### 부록
*   **표준 프롬프트를 넘어선 방법들:** 프롬프트 체이닝, 도구 사용, 검색/검색 결과 통합 등 심화 기술

## 활용 안내

*   튜토리얼은 각 장별로 반드시 **차례로 진행**하는 것을 권장합니다.
*   실전 중심의 연습과 단계별 해설로, 초보 엔지니어도 실제로 쓸 수 있는 프롬프트 설계 역량을 자연스럽게 익힐 수 있습니다.
*   모든 프로덕트 및 모델명은 원문 그대로 표기하며, 영어 기반 업무 환경에서도 바로 활용 가능합니다.

## 추가 특징 및 오픈소스 정보

*   **Github 성과:** 19,400개 이상의 Stars와 1,900개 Fork를 기록 중임
*   **개발 언어:** 주 개발 언어는 Jupyter Notebook이며, 일부 Python 코드도 포함됨
*   **배포:** 별도의 배포 패키지는 없으며, 모든 자료는 오픈소스로 자유롭게 참조 가능함

---
원문

# Welcome to Anthropic's Prompt Engineering Interactive Tutorial

## Course introduction and goals

This course is intended to provide you with a comprehensive step-by-step understanding of how to engineer optimal prompts within Claude.

**After completing this course, you will be able to**:
- Master the basic structure of a good prompt 
- Recognize common failure modes and learn the '80/20' techniques to address them
- Understand Claude's strengths and weaknesses
- Build strong prompts from scratch for common use cases

## Course structure and content

This course is structured to allow you many chances to practice writing and troubleshooting prompts yourself. The course is broken up into **9 chapters with accompanying exercises**, as well as an appendix of even more advanced methods. It is intended for you to **work through the course in chapter order**. 

**Each lesson has an "Example Playground" area** at the bottom where you are free to experiment with the examples in the lesson and see for yourself how changing prompts can change Claude's responses. There is also an [answer key](https://docs.google.com/spreadsheets/d/1jIxjzUWG-6xBVIa2ay6yDpLyeuOh_hR_ZB75a47KX_E/edit?usp=sharing).

Note: This tutorial uses our smallest, fastest, and cheapest model, Claude 3 Haiku. Anthropic has [two other models](https://docs.anthropic.com/claude/docs/models-overview), Claude 3 Sonnet and Claude 3 Opus, which are more intelligent than Haiku, with Opus being the most intelligent.

*This tutorial also exists on [Google Sheets using Anthropic's Claude for Sheets extension](https://docs.google.com/spreadsheets/d/19jzLgRruG9kjUQNKtCg1ZjdD6l6weA6qRXG5zLIAhC8/edit?usp=sharing). We recommend using that version as it is more user friendly.*

When you are ready to begin, go to `01_Basic Prompt Structure` to proceed.

## Table of Contents

Each chapter consists of a lesson and a set of exercises.

### Beginner
- **Chapter 1:** Basic Prompt Structure

- **Chapter 2:** Being Clear and Direct  

- **Chapter 3:** Assigning Roles

### Intermediate 
- **Chapter 4:** Separating Data from Instructions

- **Chapter 5:** Formatting Output & Speaking for Claude

- **Chapter 6:** Precognition (Thinking Step by Step)

- **Chapter 7:** Using Examples

### Advanced
- **Chapter 8:** Avoiding Hallucinations

- **Chapter 9:** Building Complex Prompts (Industry Use Cases)
  - Complex Prompts from Scratch - Chatbot
  - Complex Prompts for Legal Services
  - **Exercise:** Complex Prompts for Financial Services
  - **Exercise:** Complex Prompts for Coding
  - Congratulations & Next Steps

- **Appendix:** Beyond Standard Prompting
  - Chaining Prompts
  - Tool Use
  - Search & Retrieval
