---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/import-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: b54e7cf5af7eadd0ea56687a336175650b55daa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496000"
---
# <span data-ttu-id="91fc1-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="91fc1-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="91fc1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="91fc1-103">JSON-objektum importálása webszolgáltatás-definícióba.</span><span class="sxs-lookup"><span data-stu-id="91fc1-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91fc1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91fc1-104">SYNTAX</span></span>

### <span data-ttu-id="91fc1-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="91fc1-105">ImportFromJSONFile</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91fc1-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="91fc1-106">ImportFromJSONString.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91fc1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="91fc1-107">DESCRIPTION</span></span>
<span data-ttu-id="91fc1-108">A Import-AzureRmMlWebService-parancsmag a közvetlenül vagy a hivatkozott fájlban megadott formátumban, és létrehoz egy webszolgáltatás-definíciós objektumot, amely átadható a New-AzureRmMlWebService parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="91fc1-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="91fc1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="91fc1-109">EXAMPLES</span></span>

### <span data-ttu-id="91fc1-110">1. példa: importálás karakterláncból</span><span class="sxs-lookup"><span data-stu-id="91fc1-110">Example 1: Import from string</span></span>
```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="91fc1-111">2. példa: importálás fájlból útvonal</span><span class="sxs-lookup"><span data-stu-id="91fc1-111">Example 2: Import from file path</span></span>
```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="91fc1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91fc1-112">PARAMETERS</span></span>

### <span data-ttu-id="91fc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91fc1-113">-DefaultProfile</span></span>
<span data-ttu-id="91fc1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="91fc1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91fc1-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="91fc1-115">-InputFile</span></span>
<span data-ttu-id="91fc1-116">Az importálandó webszolgáltatás-definíciót tartalmazó fájl elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="91fc1-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="91fc1-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="91fc1-117">-JsonString</span></span>
<span data-ttu-id="91fc1-118">Az importálandó webszolgáltatás-definíciót tartalmazó JSON formázott karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="91fc1-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="91fc1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91fc1-119">CommonParameters</span></span>
<span data-ttu-id="91fc1-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91fc1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91fc1-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91fc1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91fc1-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91fc1-122">INPUTS</span></span>

### <span data-ttu-id="91fc1-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="91fc1-123">None</span></span>

## <span data-ttu-id="91fc1-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91fc1-124">OUTPUTS</span></span>

### <span data-ttu-id="91fc1-125">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="91fc1-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="91fc1-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91fc1-126">NOTES</span></span>
<span data-ttu-id="91fc1-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="91fc1-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="91fc1-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91fc1-128">RELATED LINKS</span></span>
