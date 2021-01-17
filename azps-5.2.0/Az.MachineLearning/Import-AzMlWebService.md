---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 90416cd786e13bdd0232aebfcff2cd6963c1f872
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360777"
---
# <span data-ttu-id="6fc15-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="6fc15-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="6fc15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fc15-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc15-103">JSON-objektumot importál egy webszolgáltatás-definícióba.</span><span class="sxs-lookup"><span data-stu-id="6fc15-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="6fc15-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6fc15-104">SYNTAX</span></span>

### <span data-ttu-id="6fc15-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="6fc15-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fc15-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="6fc15-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fc15-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6fc15-107">DESCRIPTION</span></span>
<span data-ttu-id="6fc15-108">A Import-AzMlWebService közvetlenül vagy egy hivatkozott fájlban megadott Import-AzMlWebService importál, és létrehoz egy webszolgáltatás-definíciós objektumot, amely a New-AzMlWebService parancsmagnak is át lehet adni.</span><span class="sxs-lookup"><span data-stu-id="6fc15-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="6fc15-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6fc15-109">EXAMPLES</span></span>

### <span data-ttu-id="6fc15-110">1. példa: Importálás karakterláncból</span><span class="sxs-lookup"><span data-stu-id="6fc15-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="6fc15-111">2. példa: Importálás fájl elérési útból</span><span class="sxs-lookup"><span data-stu-id="6fc15-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="6fc15-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fc15-112">PARAMETERS</span></span>

### <span data-ttu-id="6fc15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc15-113">-DefaultProfile</span></span>
<span data-ttu-id="6fc15-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6fc15-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc15-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="6fc15-115">-InputFile</span></span>
<span data-ttu-id="6fc15-116">Az importálni kívánt webszolgáltatás-definíciót tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="6fc15-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc15-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="6fc15-117">-JsonString</span></span>
<span data-ttu-id="6fc15-118">Az importálni kívánt webszolgáltatás-definíciót tartalmazó JSON formázott karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="6fc15-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONString.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc15-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc15-119">CommonParameters</span></span>
<span data-ttu-id="6fc15-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fc15-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc15-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fc15-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc15-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fc15-122">INPUTS</span></span>

### <span data-ttu-id="6fc15-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="6fc15-123">None</span></span>

## <span data-ttu-id="6fc15-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fc15-124">OUTPUTS</span></span>

### <span data-ttu-id="6fc15-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="6fc15-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="6fc15-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6fc15-126">NOTES</span></span>
<span data-ttu-id="6fc15-127">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="6fc15-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6fc15-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fc15-128">RELATED LINKS</span></span>
