---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: e722fdae30b841a92cf225f27230820fbabe4e43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942922"
---
# <span data-ttu-id="91de7-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="91de7-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="91de7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91de7-102">SYNOPSIS</span></span>
<span data-ttu-id="91de7-103">Az eseményindítók beállítása egy eszközön</span><span class="sxs-lookup"><span data-stu-id="91de7-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="91de7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="91de7-104">SYNTAX</span></span>

### <span data-ttu-id="91de7-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91de7-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91de7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91de7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91de7-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="91de7-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91de7-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91de7-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="91de7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="91de7-109">DESCRIPTION</span></span>
<span data-ttu-id="91de7-110">A **Get-AzDataBoxEdgeTriger** parancsmag kapja meg az eszköz eseményindítóit.</span><span class="sxs-lookup"><span data-stu-id="91de7-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="91de7-111">A nevet paraméterként megadhatja a parancsmagban egy adott eseményindító részleteinek lehívásakor.</span><span class="sxs-lookup"><span data-stu-id="91de7-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="91de7-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="91de7-112">EXAMPLES</span></span>

### <span data-ttu-id="91de7-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="91de7-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="91de7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91de7-114">PARAMETERS</span></span>

### <span data-ttu-id="91de7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91de7-115">-DefaultProfile</span></span>
<span data-ttu-id="91de7-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91de7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91de7-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="91de7-117">-DeviceName</span></span>
<span data-ttu-id="91de7-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="91de7-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91de7-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="91de7-119">-DeviceObject</span></span>
<span data-ttu-id="91de7-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="91de7-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91de7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="91de7-121">-Name</span></span>
<span data-ttu-id="91de7-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="91de7-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91de7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91de7-123">-ResourceGroupName</span></span>
<span data-ttu-id="91de7-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="91de7-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91de7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91de7-125">-ResourceId</span></span>
<span data-ttu-id="91de7-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="91de7-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91de7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91de7-127">CommonParameters</span></span>
<span data-ttu-id="91de7-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91de7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91de7-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91de7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91de7-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91de7-130">INPUTS</span></span>

### <span data-ttu-id="91de7-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="91de7-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="91de7-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91de7-132">OUTPUTS</span></span>

### <span data-ttu-id="91de7-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="91de7-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="91de7-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="91de7-134">NOTES</span></span>

## <span data-ttu-id="91de7-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91de7-135">RELATED LINKS</span></span>
