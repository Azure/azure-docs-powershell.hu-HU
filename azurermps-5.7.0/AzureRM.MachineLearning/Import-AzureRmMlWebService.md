---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/import-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: cc6c596b028ca7a4b89083ff06d37b3df9c3ed7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497608"
---
# <span data-ttu-id="74485-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="74485-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="74485-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74485-102">SYNOPSIS</span></span>
<span data-ttu-id="74485-103">JSON-objektum importálása webszolgáltatás-definícióba.</span><span class="sxs-lookup"><span data-stu-id="74485-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74485-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74485-104">SYNTAX</span></span>

### <span data-ttu-id="74485-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="74485-105">ImportFromJSONFile</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74485-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="74485-106">ImportFromJSONString.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74485-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="74485-107">DESCRIPTION</span></span>
<span data-ttu-id="74485-108">A Import-AzureRmMlWebService-parancsmag a közvetlenül vagy a hivatkozott fájlban megadott formátumban, és létrehoz egy webszolgáltatás-definíciós objektumot, amely átadható a New-AzureRmMlWebService parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="74485-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="74485-109">Példák</span><span class="sxs-lookup"><span data-stu-id="74485-109">EXAMPLES</span></span>

### <span data-ttu-id="74485-110">--------------------------Példa 1: importálás karakterláncból--------------------------</span><span class="sxs-lookup"><span data-stu-id="74485-110">--------------------------  Example 1: Import from string  --------------------------</span></span>
```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="74485-111">--------------------------Példa 2: importálás fájlból útvonal--------------------------</span><span class="sxs-lookup"><span data-stu-id="74485-111">--------------------------  Example 2: Import from file path  --------------------------</span></span>
```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="74485-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74485-112">PARAMETERS</span></span>

### <span data-ttu-id="74485-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74485-113">-DefaultProfile</span></span>
<span data-ttu-id="74485-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="74485-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74485-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="74485-115">-InputFile</span></span>
<span data-ttu-id="74485-116">Az importálandó webszolgáltatás-definíciót tartalmazó fájl elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="74485-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromJSONFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74485-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="74485-117">-JsonString</span></span>
<span data-ttu-id="74485-118">Az importálandó webszolgáltatás-definíciót tartalmazó JSON formázott karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="74485-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromJSONString.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74485-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74485-119">CommonParameters</span></span>
<span data-ttu-id="74485-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74485-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74485-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74485-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74485-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74485-122">INPUTS</span></span>

### <span data-ttu-id="74485-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="74485-123">None</span></span>
<span data-ttu-id="74485-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="74485-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74485-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74485-125">OUTPUTS</span></span>

### <span data-ttu-id="74485-126">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="74485-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="74485-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74485-127">NOTES</span></span>
<span data-ttu-id="74485-128">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="74485-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="74485-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74485-129">RELATED LINKS</span></span>

