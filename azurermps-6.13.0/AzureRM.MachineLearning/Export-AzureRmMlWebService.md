---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/export-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: 45e0fe4583477b05d4218f9e7b3ffb920b0218d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497388"
---
# <span data-ttu-id="a8c92-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="a8c92-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="a8c92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8c92-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c92-103">A webszolgáltatás-definíciós objektumot JSON formátumú karakterláncként exportálja.</span><span class="sxs-lookup"><span data-stu-id="a8c92-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8c92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8c92-104">SYNTAX</span></span>

### <span data-ttu-id="a8c92-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="a8c92-105">ExportToFile</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8c92-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="a8c92-106">ExportToJSON</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8c92-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8c92-107">DESCRIPTION</span></span>
<span data-ttu-id="a8c92-108">A megadott webszolga definíciós objektumának exportálása JSON formátumú karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="a8c92-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="a8c92-109">A karakterláncot azonnal visszaállíthatja, vagy fájlba mentheti.</span><span class="sxs-lookup"><span data-stu-id="a8c92-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="a8c92-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a8c92-110">EXAMPLES</span></span>

### <span data-ttu-id="a8c92-111">1. példa: exportálás karakterláncként</span><span class="sxs-lookup"><span data-stu-id="a8c92-111">Example 1: Export as string</span></span>
```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="a8c92-112">2. példa: Exportálás fájlba</span><span class="sxs-lookup"><span data-stu-id="a8c92-112">Example 2: Export to file</span></span>
```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="a8c92-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8c92-113">PARAMETERS</span></span>

### <span data-ttu-id="a8c92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c92-114">-DefaultProfile</span></span>
<span data-ttu-id="a8c92-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a8c92-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8c92-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a8c92-116">-Force</span></span>
<span data-ttu-id="a8c92-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8c92-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c92-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="a8c92-118">-OutputFile</span></span>
<span data-ttu-id="a8c92-119">Az exportált definíció fájlelérési útja.</span><span class="sxs-lookup"><span data-stu-id="a8c92-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c92-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="a8c92-120">-ToJsonString</span></span>
<span data-ttu-id="a8c92-121">Azt adja meg, hogy a definíció JSON-karakterláncként lesz exportálva.</span><span class="sxs-lookup"><span data-stu-id="a8c92-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c92-122">-Webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="a8c92-122">-WebService</span></span>
<span data-ttu-id="a8c92-123">Az exportálandó webszolgáltatás-definíciós objektum.</span><span class="sxs-lookup"><span data-stu-id="a8c92-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8c92-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8c92-124">-Confirm</span></span>
<span data-ttu-id="a8c92-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8c92-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c92-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8c92-126">-WhatIf</span></span>
<span data-ttu-id="a8c92-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a8c92-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8c92-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8c92-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8c92-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c92-129">CommonParameters</span></span>
<span data-ttu-id="a8c92-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8c92-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c92-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8c92-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c92-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8c92-132">INPUTS</span></span>

### <span data-ttu-id="a8c92-133">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="a8c92-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="a8c92-134">Paraméterek: webszolgáltatás (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a8c92-134">Parameters: WebService (ByValue)</span></span>

## <span data-ttu-id="a8c92-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8c92-135">OUTPUTS</span></span>

### <span data-ttu-id="a8c92-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a8c92-136">System.String</span></span>

## <span data-ttu-id="a8c92-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8c92-137">NOTES</span></span>
<span data-ttu-id="a8c92-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="a8c92-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a8c92-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8c92-139">RELATED LINKS</span></span>
