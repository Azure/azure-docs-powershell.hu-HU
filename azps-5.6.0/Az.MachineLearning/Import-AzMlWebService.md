---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: e30ecc151da5e4a202b8da63f8d57a8f25c387dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923553"
---
# <span data-ttu-id="316cf-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="316cf-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="316cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="316cf-102">SYNOPSIS</span></span>
<span data-ttu-id="316cf-103">JSON-objektumot importál egy webszolgáltatás-definícióba.</span><span class="sxs-lookup"><span data-stu-id="316cf-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="316cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="316cf-104">SYNTAX</span></span>

### <span data-ttu-id="316cf-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="316cf-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="316cf-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="316cf-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="316cf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="316cf-107">DESCRIPTION</span></span>
<span data-ttu-id="316cf-108">A Import-AzMlWebService közvetlenül vagy egy hivatkozott fájlban megadott Import-AzMlWebService importál, és létrehoz egy webszolgáltatás-definíciós objektumot, amely a New-AzMlWebService parancsmagnak is át lehet adni.</span><span class="sxs-lookup"><span data-stu-id="316cf-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="316cf-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="316cf-109">EXAMPLES</span></span>

### <span data-ttu-id="316cf-110">1. példa: Importálás karakterláncból</span><span class="sxs-lookup"><span data-stu-id="316cf-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="316cf-111">2. példa: Importálás fájl elérési útból</span><span class="sxs-lookup"><span data-stu-id="316cf-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="316cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="316cf-112">PARAMETERS</span></span>

### <span data-ttu-id="316cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316cf-113">-DefaultProfile</span></span>
<span data-ttu-id="316cf-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="316cf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="316cf-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="316cf-115">-InputFile</span></span>
<span data-ttu-id="316cf-116">Az importálni kívánt webszolgáltatás-definíciót tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="316cf-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="316cf-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="316cf-117">-JsonString</span></span>
<span data-ttu-id="316cf-118">Az importálni kívánt webszolgáltatás-definíciót tartalmazó JSON formázott karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="316cf-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="316cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316cf-119">CommonParameters</span></span>
<span data-ttu-id="316cf-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="316cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316cf-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="316cf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316cf-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="316cf-122">INPUTS</span></span>

### <span data-ttu-id="316cf-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="316cf-123">None</span></span>

## <span data-ttu-id="316cf-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="316cf-124">OUTPUTS</span></span>

### <span data-ttu-id="316cf-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="316cf-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="316cf-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="316cf-126">NOTES</span></span>
<span data-ttu-id="316cf-127">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="316cf-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="316cf-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="316cf-128">RELATED LINKS</span></span>
