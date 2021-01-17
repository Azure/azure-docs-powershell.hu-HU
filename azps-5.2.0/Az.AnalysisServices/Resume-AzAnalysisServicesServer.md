---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 3614c62af825b109b224d231d89dda315a7e2616
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338802"
---
# <span data-ttu-id="e101d-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e101d-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="e101d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e101d-102">SYNOPSIS</span></span>
<span data-ttu-id="e101d-103">Az Analysis Services-kiszolgáló példányának folytatása</span><span class="sxs-lookup"><span data-stu-id="e101d-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="e101d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e101d-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e101d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e101d-105">DESCRIPTION</span></span>
<span data-ttu-id="e101d-106">A Resume-AzAnalysisServicesServer parancsmag folytatja az Analysis Services-kiszolgáló egy példányát</span><span class="sxs-lookup"><span data-stu-id="e101d-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="e101d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e101d-107">EXAMPLES</span></span>

### <span data-ttu-id="e101d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e101d-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="e101d-109">Ez a parancs egy tesztkiszolgáló nevű szüneteltetett kiszolgálót folytat az erőforráscsoport tesztcsoportban</span><span class="sxs-lookup"><span data-stu-id="e101d-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="e101d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e101d-110">PARAMETERS</span></span>

### <span data-ttu-id="e101d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e101d-111">-DefaultProfile</span></span>
<span data-ttu-id="e101d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e101d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e101d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e101d-113">-Name</span></span>
<span data-ttu-id="e101d-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="e101d-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e101d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e101d-115">-PassThru</span></span>
<span data-ttu-id="e101d-116">A törölt kiszolgáló adatait adja vissza, ha a művelet sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="e101d-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="e101d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e101d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e101d-118">Annak az Azure-erőforráscsoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="e101d-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e101d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e101d-119">-Confirm</span></span>
<span data-ttu-id="e101d-120">Arra kéri a felhasználót, hogy erősítse meg a művelet elvégzését</span><span class="sxs-lookup"><span data-stu-id="e101d-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="e101d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e101d-121">-WhatIf</span></span>
<span data-ttu-id="e101d-122">Az aktuális művelet által ténylegesen végrehajtott műveleteket ismerteti anélkül, hogy végrehajtaná őket.</span><span class="sxs-lookup"><span data-stu-id="e101d-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="e101d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e101d-123">CommonParameters</span></span>
<span data-ttu-id="e101d-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e101d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e101d-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e101d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e101d-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e101d-126">INPUTS</span></span>

### <span data-ttu-id="e101d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e101d-127">System.String</span></span>

## <span data-ttu-id="e101d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e101d-128">OUTPUTS</span></span>

### <span data-ttu-id="e101d-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e101d-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="e101d-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e101d-130">NOTES</span></span>
<span data-ttu-id="e101d-131">Alias: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="e101d-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="e101d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e101d-132">RELATED LINKS</span></span>

[<span data-ttu-id="e101d-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e101d-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="e101d-134">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="e101d-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
