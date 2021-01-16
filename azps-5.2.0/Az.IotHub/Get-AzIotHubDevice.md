---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330005"
---
# <span data-ttu-id="236bf-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="236bf-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="236bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="236bf-102">SYNOPSIS</span></span>
<span data-ttu-id="236bf-103">Az Azure IoT-központban található összes eszköz vagy eszköz listája.</span><span class="sxs-lookup"><span data-stu-id="236bf-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="236bf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="236bf-104">SYNTAX</span></span>

### <span data-ttu-id="236bf-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="236bf-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="236bf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="236bf-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="236bf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="236bf-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="236bf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="236bf-108">DESCRIPTION</span></span>
<span data-ttu-id="236bf-109">Az Iot Hub-eszközök részleteinek megtekintése vagy az Iot-központ összes eszközének felsorolása.</span><span class="sxs-lookup"><span data-stu-id="236bf-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="236bf-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="236bf-110">EXAMPLES</span></span>

### <span data-ttu-id="236bf-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="236bf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="236bf-112">Az Iot-központban az összes eszköz megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="236bf-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="236bf-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="236bf-113">Example 2</span></span>
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

<span data-ttu-id="236bf-114">Az IoT-központot tartalmazó eszközök részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="236bf-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="236bf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="236bf-115">PARAMETERS</span></span>

### <span data-ttu-id="236bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="236bf-116">-DefaultProfile</span></span>
<span data-ttu-id="236bf-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="236bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="236bf-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="236bf-118">-DeviceId</span></span>
<span data-ttu-id="236bf-119">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="236bf-119">Target Device Id.</span></span>

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

### <span data-ttu-id="236bf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="236bf-120">-InputObject</span></span>
<span data-ttu-id="236bf-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="236bf-121">IotHub object</span></span>

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

### <span data-ttu-id="236bf-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="236bf-122">-IotHubName</span></span>
<span data-ttu-id="236bf-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="236bf-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="236bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="236bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="236bf-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="236bf-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="236bf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="236bf-126">-ResourceId</span></span>
<span data-ttu-id="236bf-127">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="236bf-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="236bf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="236bf-128">CommonParameters</span></span>
<span data-ttu-id="236bf-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="236bf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="236bf-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="236bf-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="236bf-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="236bf-131">INPUTS</span></span>

### <span data-ttu-id="236bf-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="236bf-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="236bf-133">System.String</span><span class="sxs-lookup"><span data-stu-id="236bf-133">System.String</span></span>

## <span data-ttu-id="236bf-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="236bf-134">OUTPUTS</span></span>

### <span data-ttu-id="236bf-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="236bf-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="236bf-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span><span class="sxs-lookup"><span data-stu-id="236bf-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="236bf-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="236bf-137">NOTES</span></span>

## <span data-ttu-id="236bf-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="236bf-138">RELATED LINKS</span></span>
