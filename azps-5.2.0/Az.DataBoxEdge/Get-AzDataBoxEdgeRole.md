---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9bda923d7a0e7e999ae8368fd648ee6745cbb226
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362808"
---
# <span data-ttu-id="94ac9-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="94ac9-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="94ac9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="94ac9-103">Lehívja az eszközhöz elérhető szerepköröket.</span><span class="sxs-lookup"><span data-stu-id="94ac9-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="94ac9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94ac9-104">SYNTAX</span></span>

### <span data-ttu-id="94ac9-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94ac9-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94ac9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94ac9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94ac9-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94ac9-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94ac9-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94ac9-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="94ac9-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94ac9-109">DESCRIPTION</span></span>
<span data-ttu-id="94ac9-110">A **Get-AzDataBoxEdgeRole** parancsmag lehívja a rendelkezésre álló IoT-szerepköröket egy Data Box Edge-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="94ac9-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="94ac9-111">Megemlítheti a Name paramétert egy adott IoT-szerepkör részleteinek lekértérte.</span><span class="sxs-lookup"><span data-stu-id="94ac9-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="94ac9-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94ac9-112">EXAMPLES</span></span>

### <span data-ttu-id="94ac9-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="94ac9-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="94ac9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94ac9-114">PARAMETERS</span></span>

### <span data-ttu-id="94ac9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ac9-115">-DefaultProfile</span></span>
<span data-ttu-id="94ac9-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94ac9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94ac9-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="94ac9-117">-DeviceName</span></span>
<span data-ttu-id="94ac9-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="94ac9-118">Device Name</span></span>

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

### <span data-ttu-id="94ac9-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="94ac9-119">-DeviceObject</span></span>
<span data-ttu-id="94ac9-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="94ac9-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="94ac9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="94ac9-121">-Name</span></span>
<span data-ttu-id="94ac9-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="94ac9-122">Resource Name</span></span>

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

### <span data-ttu-id="94ac9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94ac9-123">-ResourceGroupName</span></span>
<span data-ttu-id="94ac9-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="94ac9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="94ac9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94ac9-125">-ResourceId</span></span>
<span data-ttu-id="94ac9-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="94ac9-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="94ac9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ac9-127">CommonParameters</span></span>
<span data-ttu-id="94ac9-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ac9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ac9-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94ac9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ac9-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94ac9-130">INPUTS</span></span>

### <span data-ttu-id="94ac9-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="94ac9-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="94ac9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94ac9-132">OUTPUTS</span></span>

### <span data-ttu-id="94ac9-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="94ac9-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="94ac9-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94ac9-134">NOTES</span></span>

## <span data-ttu-id="94ac9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94ac9-135">RELATED LINKS</span></span>
