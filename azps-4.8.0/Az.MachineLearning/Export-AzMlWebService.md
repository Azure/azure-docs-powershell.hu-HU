---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018195"
---
# <span data-ttu-id="a8486-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="a8486-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="a8486-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8486-102">SYNOPSIS</span></span>
<span data-ttu-id="a8486-103">A webszolgáltatás-definíciós objektumot JSON formátumú karakterláncként exportálja.</span><span class="sxs-lookup"><span data-stu-id="a8486-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="a8486-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8486-104">SYNTAX</span></span>

### <span data-ttu-id="a8486-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="a8486-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8486-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="a8486-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8486-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8486-107">DESCRIPTION</span></span>
<span data-ttu-id="a8486-108">A megadott webszolgáltatáshoz tartozó definition objektum exportálása JSON formátumú karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="a8486-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="a8486-109">A karakterláncot azonnal visszaállíthatja, vagy fájlba mentheti.</span><span class="sxs-lookup"><span data-stu-id="a8486-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="a8486-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a8486-110">EXAMPLES</span></span>

### <span data-ttu-id="a8486-111">1. példa: exportálás karakterláncként</span><span class="sxs-lookup"><span data-stu-id="a8486-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="a8486-112">2. példa: Exportálás fájlba</span><span class="sxs-lookup"><span data-stu-id="a8486-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="a8486-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8486-113">PARAMETERS</span></span>

### <span data-ttu-id="a8486-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8486-114">-DefaultProfile</span></span>
<span data-ttu-id="a8486-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a8486-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8486-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a8486-116">-Force</span></span>
<span data-ttu-id="a8486-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8486-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a8486-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="a8486-118">-OutputFile</span></span>
<span data-ttu-id="a8486-119">Az exportált definíció fájlelérési útja.</span><span class="sxs-lookup"><span data-stu-id="a8486-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="a8486-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="a8486-120">-ToJsonString</span></span>
<span data-ttu-id="a8486-121">Azt adja meg, hogy a definíció JSON-karakterláncként lesz exportálva.</span><span class="sxs-lookup"><span data-stu-id="a8486-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="a8486-122">-Webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="a8486-122">-WebService</span></span>
<span data-ttu-id="a8486-123">Az exportálandó webszolgáltatás-definíciós objektum.</span><span class="sxs-lookup"><span data-stu-id="a8486-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="a8486-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8486-124">-Confirm</span></span>
<span data-ttu-id="a8486-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8486-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8486-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8486-126">-WhatIf</span></span>
<span data-ttu-id="a8486-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a8486-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8486-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8486-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8486-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8486-129">CommonParameters</span></span>
<span data-ttu-id="a8486-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8486-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8486-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8486-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8486-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8486-132">INPUTS</span></span>

### <span data-ttu-id="a8486-133">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="a8486-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="a8486-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8486-134">OUTPUTS</span></span>

### <span data-ttu-id="a8486-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a8486-135">System.String</span></span>

## <span data-ttu-id="a8486-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8486-136">NOTES</span></span>
<span data-ttu-id="a8486-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="a8486-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a8486-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8486-138">RELATED LINKS</span></span>
