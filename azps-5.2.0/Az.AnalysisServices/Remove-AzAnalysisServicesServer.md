---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: 9076df0ae023539560b690723dd9abc92d922e45
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352949"
---
# <span data-ttu-id="dbc9e-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dbc9e-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="dbc9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc9e-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc9e-103">Az Analysis Services-kiszolgáló egy példányának törlése</span><span class="sxs-lookup"><span data-stu-id="dbc9e-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="dbc9e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dbc9e-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbc9e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dbc9e-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc9e-106">A Remove-AzAnalysisServicesServer parancsmag törli az Analysis Services-kiszolgáló egy példányát</span><span class="sxs-lookup"><span data-stu-id="dbc9e-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="dbc9e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dbc9e-107">EXAMPLES</span></span>

### <span data-ttu-id="dbc9e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="dbc9e-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="dbc9e-109">Ez a parancs eltávolítja a testserver kiszolgálót az erőforráscsoport tesztcsoportban</span><span class="sxs-lookup"><span data-stu-id="dbc9e-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="dbc9e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbc9e-110">PARAMETERS</span></span>

### <span data-ttu-id="dbc9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc9e-111">-DefaultProfile</span></span>
<span data-ttu-id="dbc9e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dbc9e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbc9e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="dbc9e-113">-Name</span></span>
<span data-ttu-id="dbc9e-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="dbc9e-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="dbc9e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbc9e-115">-PassThru</span></span>
<span data-ttu-id="dbc9e-116">A törölt kiszolgáló adatait adja vissza, ha a művelet sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="dbc9e-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="dbc9e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc9e-117">-ResourceGroupName</span></span>
<span data-ttu-id="dbc9e-118">Annak az Azure-erőforráscsoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="dbc9e-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="dbc9e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbc9e-119">-Confirm</span></span>
<span data-ttu-id="dbc9e-120">Arra kéri a felhasználót, hogy erősítse meg a művelet elvégzését</span><span class="sxs-lookup"><span data-stu-id="dbc9e-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="dbc9e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbc9e-121">-WhatIf</span></span>
<span data-ttu-id="dbc9e-122">Az aktuális művelet által ténylegesen végrehajtott műveleteket ismerteti anélkül, hogy végrehajtaná őket.</span><span class="sxs-lookup"><span data-stu-id="dbc9e-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="dbc9e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc9e-123">CommonParameters</span></span>
<span data-ttu-id="dbc9e-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc9e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc9e-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbc9e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc9e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbc9e-126">INPUTS</span></span>

### <span data-ttu-id="dbc9e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="dbc9e-127">System.String</span></span>

## <span data-ttu-id="dbc9e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbc9e-128">OUTPUTS</span></span>

### <span data-ttu-id="dbc9e-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dbc9e-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="dbc9e-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dbc9e-130">NOTES</span></span>
<span data-ttu-id="dbc9e-131">Alias: Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="dbc9e-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="dbc9e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbc9e-132">RELATED LINKS</span></span>

[<span data-ttu-id="dbc9e-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dbc9e-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="dbc9e-134">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dbc9e-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)
