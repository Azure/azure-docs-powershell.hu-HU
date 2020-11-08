---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183838"
---
# <span data-ttu-id="637b5-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="637b5-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="637b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="637b5-102">SYNOPSIS</span></span>
<span data-ttu-id="637b5-103">Az eszközhöz elérhető szerepkörök beolvasása.</span><span class="sxs-lookup"><span data-stu-id="637b5-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="637b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="637b5-104">SYNTAX</span></span>

### <span data-ttu-id="637b5-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="637b5-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="637b5-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="637b5-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="637b5-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="637b5-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="637b5-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="637b5-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="637b5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="637b5-109">DESCRIPTION</span></span>
<span data-ttu-id="637b5-110">A **Get-AzStackEdgeRole** parancsmag beolvassa az elérhető IoT-szerepköröket egy halom Edge-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="637b5-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="637b5-111">Megemlítheti a Name (név) paramétert egy adott IoT szerepkör részleteinek megadásához.</span><span class="sxs-lookup"><span data-stu-id="637b5-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="637b5-112">Példák</span><span class="sxs-lookup"><span data-stu-id="637b5-112">EXAMPLES</span></span>

### <span data-ttu-id="637b5-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="637b5-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="637b5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="637b5-114">PARAMETERS</span></span>

### <span data-ttu-id="637b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="637b5-115">-DefaultProfile</span></span>
<span data-ttu-id="637b5-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="637b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="637b5-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="637b5-117">-DeviceName</span></span>
<span data-ttu-id="637b5-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="637b5-118">Device Name</span></span>

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

### <span data-ttu-id="637b5-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="637b5-119">-DeviceObject</span></span>
<span data-ttu-id="637b5-120">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="637b5-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="637b5-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="637b5-121">-Name</span></span>
<span data-ttu-id="637b5-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="637b5-122">Resource Name</span></span>

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

### <span data-ttu-id="637b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="637b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="637b5-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="637b5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="637b5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="637b5-125">-ResourceId</span></span>
<span data-ttu-id="637b5-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="637b5-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="637b5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="637b5-127">CommonParameters</span></span>
<span data-ttu-id="637b5-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="637b5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="637b5-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="637b5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="637b5-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="637b5-130">INPUTS</span></span>

### <span data-ttu-id="637b5-131">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="637b5-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="637b5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="637b5-132">OUTPUTS</span></span>

### <span data-ttu-id="637b5-133">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="637b5-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="637b5-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="637b5-134">NOTES</span></span>

## <span data-ttu-id="637b5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="637b5-135">RELATED LINKS</span></span>
