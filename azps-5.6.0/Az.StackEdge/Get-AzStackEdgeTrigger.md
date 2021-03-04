---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: a4bcbad5f595efe126ed232b94d5deb368515bc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930737"
---
# <span data-ttu-id="b2060-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="b2060-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="b2060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2060-102">SYNOPSIS</span></span>
<span data-ttu-id="b2060-103">Az eseményindítók beállítása egy eszközön</span><span class="sxs-lookup"><span data-stu-id="b2060-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="b2060-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b2060-104">SYNTAX</span></span>

### <span data-ttu-id="b2060-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2060-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2060-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2060-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2060-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2060-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2060-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2060-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="b2060-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b2060-109">DESCRIPTION</span></span>
<span data-ttu-id="b2060-110">A **Get-AzStackEdgeTriger** parancsmag kapja meg az eszköz eseményindítóit.</span><span class="sxs-lookup"><span data-stu-id="b2060-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="b2060-111">A nevet paraméterként megadhatja a parancsmagban egy adott eseményindító részleteinek lehívásakor.</span><span class="sxs-lookup"><span data-stu-id="b2060-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="b2060-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b2060-112">EXAMPLES</span></span>

### <span data-ttu-id="b2060-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="b2060-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="b2060-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2060-114">PARAMETERS</span></span>

### <span data-ttu-id="b2060-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2060-115">-DefaultProfile</span></span>
<span data-ttu-id="b2060-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2060-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2060-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b2060-117">-DeviceName</span></span>
<span data-ttu-id="b2060-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="b2060-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2060-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="b2060-119">-DeviceObject</span></span>
<span data-ttu-id="b2060-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="b2060-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2060-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b2060-121">-Name</span></span>
<span data-ttu-id="b2060-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="b2060-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2060-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2060-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2060-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b2060-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2060-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2060-125">-ResourceId</span></span>
<span data-ttu-id="b2060-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2060-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2060-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2060-127">CommonParameters</span></span>
<span data-ttu-id="b2060-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2060-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2060-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2060-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2060-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2060-130">INPUTS</span></span>

### <span data-ttu-id="b2060-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b2060-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="b2060-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2060-132">OUTPUTS</span></span>

### <span data-ttu-id="b2060-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="b2060-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="b2060-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b2060-134">NOTES</span></span>

## <span data-ttu-id="b2060-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2060-135">RELATED LINKS</span></span>
