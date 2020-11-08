---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011897"
---
# <span data-ttu-id="5c3a4-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="5c3a4-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="5c3a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c3a4-102">SYNOPSIS</span></span>
<span data-ttu-id="5c3a4-103">Az Azure IoT-központban található összes eszköz vagy egy adott eszköz felsorolása.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="5c3a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c3a4-104">SYNTAX</span></span>

### <span data-ttu-id="5c3a4-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5c3a4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c3a4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5c3a4-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c3a4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5c3a4-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c3a4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c3a4-108">DESCRIPTION</span></span>
<span data-ttu-id="5c3a4-109">Megtudhatja, hogy miként szerezheti be a IOT hub-eszközök adatait, vagy egy IOT-hub összes eszközét felsorolhatja.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="5c3a4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5c3a4-110">EXAMPLES</span></span>

### <span data-ttu-id="5c3a4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5c3a4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="5c3a4-112">Az IOT-hub minden eszközének megjelenítése</span><span class="sxs-lookup"><span data-stu-id="5c3a4-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="5c3a4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5c3a4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Disabled
StatusReason               : Reason1
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                :
```

<span data-ttu-id="5c3a4-114">Megtudhatja, hogy miként szerezheti be a IoT hub eszköz adatait.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="5c3a4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c3a4-115">PARAMETERS</span></span>

### <span data-ttu-id="5c3a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c3a4-116">-DefaultProfile</span></span>
<span data-ttu-id="5c3a4-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c3a4-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5c3a4-118">-DeviceId</span></span>
<span data-ttu-id="5c3a4-119">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5c3a4-119">Target Device Id.</span></span>

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

### <span data-ttu-id="5c3a4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c3a4-120">-InputObject</span></span>
<span data-ttu-id="5c3a4-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="5c3a4-121">IotHub object</span></span>

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

### <span data-ttu-id="5c3a4-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5c3a4-122">-IotHubName</span></span>
<span data-ttu-id="5c3a4-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="5c3a4-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5c3a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c3a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c3a4-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5c3a4-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5c3a4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c3a4-126">-ResourceId</span></span>
<span data-ttu-id="5c3a4-127">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="5c3a4-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5c3a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c3a4-128">CommonParameters</span></span>
<span data-ttu-id="5c3a4-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c3a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c3a4-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c3a4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c3a4-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c3a4-131">INPUTS</span></span>

### <span data-ttu-id="5c3a4-132">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5c3a4-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5c3a4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5c3a4-133">System.String</span></span>

## <span data-ttu-id="5c3a4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c3a4-134">OUTPUTS</span></span>

### <span data-ttu-id="5c3a4-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEvice</span><span class="sxs-lookup"><span data-stu-id="5c3a4-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="5c3a4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeszközökhöz []</span><span class="sxs-lookup"><span data-stu-id="5c3a4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="5c3a4-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c3a4-137">NOTES</span></span>

## <span data-ttu-id="5c3a4-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c3a4-138">RELATED LINKS</span></span>
