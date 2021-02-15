---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207287"
---
# <span data-ttu-id="aa26d-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="aa26d-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="aa26d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa26d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa26d-103">A webszolgáltatás-definíciós objektumot JSON formátumú karakterláncként exportálja.</span><span class="sxs-lookup"><span data-stu-id="aa26d-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="aa26d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aa26d-104">SYNTAX</span></span>

### <span data-ttu-id="aa26d-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="aa26d-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa26d-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="aa26d-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa26d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aa26d-107">DESCRIPTION</span></span>
<span data-ttu-id="aa26d-108">A megadott webszolgáltatás definíciós objektumát JSON formátumú karakterláncként exportálja.</span><span class="sxs-lookup"><span data-stu-id="aa26d-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="aa26d-109">A karakterláncot azonnal vissza is használhatja, vagy mentheti egy fájlba.</span><span class="sxs-lookup"><span data-stu-id="aa26d-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="aa26d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aa26d-110">EXAMPLES</span></span>

### <span data-ttu-id="aa26d-111">1. példa: Exportálás karakterláncként</span><span class="sxs-lookup"><span data-stu-id="aa26d-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="aa26d-112">2. példa: Exportálás fájlba</span><span class="sxs-lookup"><span data-stu-id="aa26d-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="aa26d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa26d-113">PARAMETERS</span></span>

### <span data-ttu-id="aa26d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa26d-114">-DefaultProfile</span></span>
<span data-ttu-id="aa26d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aa26d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa26d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="aa26d-116">-Force</span></span>
<span data-ttu-id="aa26d-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa26d-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="aa26d-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="aa26d-118">-OutputFile</span></span>
<span data-ttu-id="aa26d-119">Az exportált definíció fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="aa26d-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="aa26d-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="aa26d-120">-ToJsonString</span></span>
<span data-ttu-id="aa26d-121">Azt adja meg, hogy a definíció JSON-karakterláncként lesz exportálva.</span><span class="sxs-lookup"><span data-stu-id="aa26d-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="aa26d-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="aa26d-122">-WebService</span></span>
<span data-ttu-id="aa26d-123">Az exportálni célként használt webszolgáltatás-definíciós objektum.</span><span class="sxs-lookup"><span data-stu-id="aa26d-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="aa26d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa26d-124">-Confirm</span></span>
<span data-ttu-id="aa26d-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aa26d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa26d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa26d-126">-WhatIf</span></span>
<span data-ttu-id="aa26d-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aa26d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa26d-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa26d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa26d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa26d-129">CommonParameters</span></span>
<span data-ttu-id="aa26d-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa26d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa26d-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa26d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa26d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa26d-132">INPUTS</span></span>

### <span data-ttu-id="aa26d-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="aa26d-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="aa26d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa26d-134">OUTPUTS</span></span>

### <span data-ttu-id="aa26d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="aa26d-135">System.String</span></span>

## <span data-ttu-id="aa26d-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aa26d-136">NOTES</span></span>
<span data-ttu-id="aa26d-137">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, gépi, gépi tanulás, azureml</span><span class="sxs-lookup"><span data-stu-id="aa26d-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="aa26d-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa26d-138">RELATED LINKS</span></span>
