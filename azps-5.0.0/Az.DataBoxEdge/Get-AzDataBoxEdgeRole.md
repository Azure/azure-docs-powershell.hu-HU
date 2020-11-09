---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9bda923d7a0e7e999ae8368fd648ee6745cbb226
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298850"
---
# <span data-ttu-id="e0285-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e0285-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="e0285-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0285-102">SYNOPSIS</span></span>
<span data-ttu-id="e0285-103">Az eszközhöz elérhető szerepkörök beolvasása.</span><span class="sxs-lookup"><span data-stu-id="e0285-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="e0285-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0285-104">SYNTAX</span></span>

### <span data-ttu-id="e0285-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0285-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0285-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0285-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0285-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0285-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0285-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0285-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="e0285-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0285-109">DESCRIPTION</span></span>
<span data-ttu-id="e0285-110">A **Get-AzDataBoxEdgeRole** parancsmag lekérdezi az IoT-szerepköröket az adatmező szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="e0285-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="e0285-111">Megemlítheti a Name (név) paramétert egy adott IoT szerepkör részleteinek megadásához.</span><span class="sxs-lookup"><span data-stu-id="e0285-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="e0285-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e0285-112">EXAMPLES</span></span>

### <span data-ttu-id="e0285-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e0285-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="e0285-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0285-114">PARAMETERS</span></span>

### <span data-ttu-id="e0285-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0285-115">-DefaultProfile</span></span>
<span data-ttu-id="e0285-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0285-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0285-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e0285-117">-DeviceName</span></span>
<span data-ttu-id="e0285-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="e0285-118">Device Name</span></span>

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

### <span data-ttu-id="e0285-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e0285-119">-DeviceObject</span></span>
<span data-ttu-id="e0285-120">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="e0285-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="e0285-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0285-121">-Name</span></span>
<span data-ttu-id="e0285-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="e0285-122">Resource Name</span></span>

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

### <span data-ttu-id="e0285-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0285-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0285-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e0285-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e0285-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0285-125">-ResourceId</span></span>
<span data-ttu-id="e0285-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0285-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="e0285-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0285-127">CommonParameters</span></span>
<span data-ttu-id="e0285-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0285-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0285-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0285-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0285-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0285-130">INPUTS</span></span>

### <span data-ttu-id="e0285-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e0285-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="e0285-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0285-132">OUTPUTS</span></span>

### <span data-ttu-id="e0285-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e0285-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="e0285-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0285-134">NOTES</span></span>

## <span data-ttu-id="e0285-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0285-135">RELATED LINKS</span></span>
