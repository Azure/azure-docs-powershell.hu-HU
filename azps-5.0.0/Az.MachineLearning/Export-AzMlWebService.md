---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195827"
---
# <span data-ttu-id="7dd34-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="7dd34-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="7dd34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7dd34-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd34-103">A webszolgáltatás-definíciós objektumot JSON formátumú karakterláncként exportálja.</span><span class="sxs-lookup"><span data-stu-id="7dd34-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="7dd34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7dd34-104">SYNTAX</span></span>

### <span data-ttu-id="7dd34-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="7dd34-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dd34-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="7dd34-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dd34-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7dd34-107">DESCRIPTION</span></span>
<span data-ttu-id="7dd34-108">A megadott webszolgáltatáshoz tartozó definition objektum exportálása JSON formátumú karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="7dd34-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="7dd34-109">A karakterláncot azonnal visszaállíthatja, vagy fájlba mentheti.</span><span class="sxs-lookup"><span data-stu-id="7dd34-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="7dd34-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7dd34-110">EXAMPLES</span></span>

### <span data-ttu-id="7dd34-111">1. példa: exportálás karakterláncként</span><span class="sxs-lookup"><span data-stu-id="7dd34-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="7dd34-112">2. példa: Exportálás fájlba</span><span class="sxs-lookup"><span data-stu-id="7dd34-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="7dd34-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7dd34-113">PARAMETERS</span></span>

### <span data-ttu-id="7dd34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd34-114">-DefaultProfile</span></span>
<span data-ttu-id="7dd34-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7dd34-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7dd34-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7dd34-116">-Force</span></span>
<span data-ttu-id="7dd34-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7dd34-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7dd34-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="7dd34-118">-OutputFile</span></span>
<span data-ttu-id="7dd34-119">Az exportált definíció fájlelérési útja.</span><span class="sxs-lookup"><span data-stu-id="7dd34-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="7dd34-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="7dd34-120">-ToJsonString</span></span>
<span data-ttu-id="7dd34-121">Azt adja meg, hogy a definíció JSON-karakterláncként lesz exportálva.</span><span class="sxs-lookup"><span data-stu-id="7dd34-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="7dd34-122">-Webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="7dd34-122">-WebService</span></span>
<span data-ttu-id="7dd34-123">Az exportálandó webszolgáltatás-definíciós objektum.</span><span class="sxs-lookup"><span data-stu-id="7dd34-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="7dd34-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7dd34-124">-Confirm</span></span>
<span data-ttu-id="7dd34-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7dd34-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dd34-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dd34-126">-WhatIf</span></span>
<span data-ttu-id="7dd34-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7dd34-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dd34-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7dd34-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dd34-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd34-129">CommonParameters</span></span>
<span data-ttu-id="7dd34-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7dd34-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd34-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dd34-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd34-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7dd34-132">INPUTS</span></span>

### <span data-ttu-id="7dd34-133">Microsoft. Azure. Management. MachineLearning. WebServices. models. webszolgáltatás</span><span class="sxs-lookup"><span data-stu-id="7dd34-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="7dd34-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7dd34-134">OUTPUTS</span></span>

### <span data-ttu-id="7dd34-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7dd34-135">System.String</span></span>

## <span data-ttu-id="7dd34-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7dd34-136">NOTES</span></span>
<span data-ttu-id="7dd34-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, gép, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="7dd34-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7dd34-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7dd34-138">RELATED LINKS</span></span>