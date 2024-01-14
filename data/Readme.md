## Dataset

As a part of the dataset we provide three files

1. Annotated cases of 122 documents pairs present in file: annotated_spans (unzip and you get file: annotated_spans.jsonl)
2. List of inspected documents and their additional data is in: "inspected_documents.xlsx"
3. List of potential source documents for the inspected documents and their additional data is in: "potsrc_documents.xlsx"

## Annotated Span 

We used TEIMMA to annotate pairs of spans (a case) from inspected documents and their potential source documents. A typical case has following format and information with it:

```
	jsonDocinfo = {
	inspecDoc: {inspecDocName: insepc_1.txt, inspecText: The text that is reused from potential source document,
					inspecMath: [iM1, iM2], inspecImages: [iImg1, iImg2],
					inspecDocHTML: selected reuse span in HTML,
					inspecDocHTMLParent: parent HTML span of reused span in HTML
					},
	potsrcDoc": {potsrcDocName: src_1.txt, "potsrcText": Resued text from potential source document,
					potsrcMath: [sM1, sM2], "potsrcImages": [sImg1, sImg2],
					potsrcDocHTML: selected reuse span in HTML,
					potsrcDocHTMLParent: parent HTML span of reused span in HTML
					},
	"colorHighlight": Blue	
	}
	recordings = {"inspecDocstart": span_character_position, "inspecDocend": span_character_position,
					"potsrcDocstart": span_character_position, "potsrcDocend": span_character_position,
					"obfuscation":[P/TMMT/S/DP/VS/FM/ID], "recordingType":Text/Math/Images
					}
	}
```

- Recording spans (Example: inspecDocstart, inspecDocend) are ontained by taking full text of the insepc_1 doc 

## Obtaining full texts 

We extracted information about documents identified for noticeable content reuse at zbMATH Open.
The file "annotations_withIDs.jsonl" also contains documents under inspection and source document's zbMATH IDs.
One can search these IDs directly on zbMATH.org and obtain its metadata or from the above provided files.
To download the full texts in PDF or LaTeX format, please click on provided link on zbMATH website or simplay search the title in pospular repositories.
For converting PDF to LaTeX please use MathPiX.