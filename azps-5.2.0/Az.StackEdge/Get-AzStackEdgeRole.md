---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359125"
---
# <span data-ttu-id="33639-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="33639-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="33639-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33639-102">SYNOPSIS</span></span>
<span data-ttu-id="33639-103">Lehívja az eszközhöz elérhető szerepköröket.</span><span class="sxs-lookup"><span data-stu-id="33639-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="33639-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="33639-104">SYNTAX</span></span>

### <span data-ttu-id="33639-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33639-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33639-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33639-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33639-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="33639-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33639-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33639-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="33639-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="33639-109">DESCRIPTION</span></span>
<span data-ttu-id="33639-110">A **Get-AzStackEdgeRole** parancsmag lehívja a stack edge-es eszközök rendelkezésre álló IoT-szerepköreit.</span><span class="sxs-lookup"><span data-stu-id="33639-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="33639-111">Megemlítheti a Name paramétert egy adott IoT-szerepkör részleteinek lekértérte.</span><span class="sxs-lookup"><span data-stu-id="33639-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="33639-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="33639-112">EXAMPLES</span></span>

### <span data-ttu-id="33639-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="33639-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="33639-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33639-114">PARAMETERS</span></span>

### <span data-ttu-id="33639-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33639-115">-DefaultProfile</span></span>
<span data-ttu-id="33639-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33639-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33639-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="33639-117">-DeviceName</span></span>
<span data-ttu-id="33639-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="33639-118">Device Name</span></span>

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

### <span data-ttu-id="33639-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="33639-119">-DeviceObject</span></span>
<span data-ttu-id="33639-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="33639-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="33639-121">-Name</span><span class="sxs-lookup"><span data-stu-id="33639-121">-Name</span></span>
<span data-ttu-id="33639-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="33639-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: RoleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33639-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33639-123">-ResourceGroupName</span></span>
<span data-ttu-id="33639-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="33639-124">Resource Group Name</span></span>

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

### <span data-ttu-id="33639-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33639-125">-ResourceId</span></span>
<span data-ttu-id="33639-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="33639-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="33639-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33639-127">CommonParameters</span></span>
<span data-ttu-id="33639-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33639-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33639-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33639-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33639-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33639-130">INPUTS</span></span>

### <span data-ttu-id="33639-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="33639-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="33639-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33639-132">OUTPUTS</span></span>

### <span data-ttu-id="33639-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="33639-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="33639-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="33639-134">NOTES</span></span>

## <span data-ttu-id="33639-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33639-135">RELATED LINKS</span></span>
