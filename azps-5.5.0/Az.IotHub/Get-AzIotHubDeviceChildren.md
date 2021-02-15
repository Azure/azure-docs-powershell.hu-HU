---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152987"
---
# <span data-ttu-id="c2b65-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="c2b65-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="c2b65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2b65-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b65-103">A hozzárendelt gyermekeszközök vesszővel elválasztott listájának nyomtatása.</span><span class="sxs-lookup"><span data-stu-id="c2b65-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="c2b65-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2b65-104">SYNTAX</span></span>

### <span data-ttu-id="c2b65-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2b65-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2b65-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c2b65-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2b65-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c2b65-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2b65-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2b65-108">DESCRIPTION</span></span>
<span data-ttu-id="c2b65-109">Az összes hozzárendelt, nem edge-hez rendelt eszköz megjelenítése vesszővel elválasztott listaként az összes peremhálózati eszközről vagy adott eszközről.</span><span class="sxs-lookup"><span data-stu-id="c2b65-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="c2b65-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2b65-110">EXAMPLES</span></span>

### <span data-ttu-id="c2b65-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c2b65-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="c2b65-112">Az összes hozzárendelt, nem edge-hez rendelt eszköz megjelenítése vesszővel elválasztott listaként.</span><span class="sxs-lookup"><span data-stu-id="c2b65-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="c2b65-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c2b65-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="c2b65-114">Az összes hozzárendelt, nem edge-hez rendelt eszköz megjelenítése az összes peremhálózati eszköz vesszővel elválasztott listájaként.</span><span class="sxs-lookup"><span data-stu-id="c2b65-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="c2b65-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2b65-115">PARAMETERS</span></span>

### <span data-ttu-id="c2b65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b65-116">-DefaultProfile</span></span>
<span data-ttu-id="c2b65-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2b65-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2b65-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c2b65-118">-DeviceId</span></span>
<span data-ttu-id="c2b65-119">A peremhálózati eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c2b65-119">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b65-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2b65-120">-InputObject</span></span>
<span data-ttu-id="c2b65-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="c2b65-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b65-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c2b65-122">-IotHubName</span></span>
<span data-ttu-id="c2b65-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="c2b65-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b65-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b65-124">-ResourceGroupName</span></span>
<span data-ttu-id="c2b65-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c2b65-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b65-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2b65-126">-ResourceId</span></span>
<span data-ttu-id="c2b65-127">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c2b65-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b65-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b65-128">CommonParameters</span></span>
<span data-ttu-id="c2b65-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b65-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b65-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b65-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b65-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2b65-131">INPUTS</span></span>

### <span data-ttu-id="c2b65-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c2b65-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c2b65-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c2b65-133">System.String</span></span>

## <span data-ttu-id="c2b65-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2b65-134">OUTPUTS</span></span>

### <span data-ttu-id="c2b65-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice Minden</span><span class="sxs-lookup"><span data-stu-id="c2b65-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="c2b65-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesKv[]</span><span class="sxs-lookup"><span data-stu-id="c2b65-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="c2b65-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2b65-137">NOTES</span></span>

## <span data-ttu-id="c2b65-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2b65-138">RELATED LINKS</span></span>
