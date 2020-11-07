---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 7c885da5423e765cca3d18ce18957c0e64bb2c36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835301"
---
# <span data-ttu-id="e2848-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="e2848-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="e2848-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2848-102">SYNOPSIS</span></span>
<span data-ttu-id="e2848-103">JSON-objektum importálása webszolgáltatás-definícióba.</span><span class="sxs-lookup"><span data-stu-id="e2848-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="e2848-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2848-104">SYNTAX</span></span>

### <span data-ttu-id="e2848-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="e2848-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2848-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="e2848-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2848-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2848-107">DESCRIPTION</span></span>
<span data-ttu-id="e2848-108">A Import-AzMlWebService-parancsmag a közvetlenül vagy a hivatkozott fájlban megadott formátumban, és létrehoz egy webszolgáltatás-definíciós objektumot, amely átadható a New-AzMlWebService parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="e2848-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="e2848-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e2848-109">EXAMPLES</span></span>

### <span data-ttu-id="e2848-110">1. példa: importálás karakterláncból</span><span class="sxs-lookup"><span data-stu-id="e2848-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="e2848-111">2. példa: importálás fájlból útvonal</span><span class="sxs-lookup"><span data-stu-id="e2848-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="e2848-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2848-112">PARAMETERS</span></span>

### <span data-ttu-id="e2848-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2848-113">-DefaultProfile</span></span>
<span data-ttu-id="e2848-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e2848-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2848-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="e2848-115">-InputFile</span></span>
<span data-ttu-id="e2848-116">Az importálandó webszolgáltatás-definíciót tartalmazó fájl elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="e2848-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="e2848-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="e2848-117">-JsonString</span></span>
<span data-ttu-id="e2848-118">Az importálandó webszolgáltatás-definíciót tartalmazó JSON formázott karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="e2848-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="e2848-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2848-119">CommonParameters</span></span>
<span data-ttu-id="e2848-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2848-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2848-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2848-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2848-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2848-122">INPUTS</span></span>

### <span data-ttu-id="e2848-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="e2848-123">None</span></span>

## <span data-ttu-id="e2848-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2848-124">OUTPUTS</span></span>

### <span data-ttu-id="e2848-125">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="e2848-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="e2848-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2848-126">NOTES</span></span>
<span data-ttu-id="e2848-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="e2848-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e2848-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2848-128">RELATED LINKS</span></span>
