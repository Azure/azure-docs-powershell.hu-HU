---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: 9076df0ae023539560b690723dd9abc92d922e45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205863"
---
# <span data-ttu-id="0adb3-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0adb3-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="0adb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0adb3-102">SYNOPSIS</span></span>
<span data-ttu-id="0adb3-103">Az Analysis Services-kiszolgáló egy példányának törlése</span><span class="sxs-lookup"><span data-stu-id="0adb3-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="0adb3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0adb3-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0adb3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0adb3-105">DESCRIPTION</span></span>
<span data-ttu-id="0adb3-106">A Remove-AzAnalysisServicesServer parancsmag törli az Analysis Services-kiszolgáló egy példányát</span><span class="sxs-lookup"><span data-stu-id="0adb3-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="0adb3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0adb3-107">EXAMPLES</span></span>

### <span data-ttu-id="0adb3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0adb3-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="0adb3-109">Ez a parancs eltávolítja a testserver kiszolgálót az erőforráscsoport tesztcsoportban</span><span class="sxs-lookup"><span data-stu-id="0adb3-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="0adb3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0adb3-110">PARAMETERS</span></span>

### <span data-ttu-id="0adb3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0adb3-111">-DefaultProfile</span></span>
<span data-ttu-id="0adb3-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0adb3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0adb3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0adb3-113">-Name</span></span>
<span data-ttu-id="0adb3-114">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="0adb3-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="0adb3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0adb3-115">-PassThru</span></span>
<span data-ttu-id="0adb3-116">A törölt kiszolgáló adatait adja vissza, ha a művelet sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="0adb3-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="0adb3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0adb3-117">-ResourceGroupName</span></span>
<span data-ttu-id="0adb3-118">Annak az Azure-erőforráscsoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="0adb3-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="0adb3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0adb3-119">-Confirm</span></span>
<span data-ttu-id="0adb3-120">Arra kéri a felhasználót, hogy erősítse meg a művelet elvégzését</span><span class="sxs-lookup"><span data-stu-id="0adb3-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="0adb3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0adb3-121">-WhatIf</span></span>
<span data-ttu-id="0adb3-122">Az aktuális művelet által ténylegesen végrehajtott műveleteket ismerteti anélkül, hogy végrehajtaná őket.</span><span class="sxs-lookup"><span data-stu-id="0adb3-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="0adb3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0adb3-123">CommonParameters</span></span>
<span data-ttu-id="0adb3-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0adb3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0adb3-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0adb3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0adb3-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0adb3-126">INPUTS</span></span>

### <span data-ttu-id="0adb3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0adb3-127">System.String</span></span>

## <span data-ttu-id="0adb3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0adb3-128">OUTPUTS</span></span>

### <span data-ttu-id="0adb3-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0adb3-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="0adb3-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0adb3-130">NOTES</span></span>
<span data-ttu-id="0adb3-131">Alias: Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="0adb3-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="0adb3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0adb3-132">RELATED LINKS</span></span>

[<span data-ttu-id="0adb3-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0adb3-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="0adb3-134">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0adb3-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)
