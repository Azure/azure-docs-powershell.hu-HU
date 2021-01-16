---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329981"
---
# <span data-ttu-id="1ba78-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="1ba78-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="1ba78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ba78-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba78-103">Szerezze be egy cél IoT-eszköz kapcsolati karakterláncát egy Iot-központban.</span><span class="sxs-lookup"><span data-stu-id="1ba78-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="1ba78-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ba78-104">SYNTAX</span></span>

### <span data-ttu-id="1ba78-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ba78-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ba78-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1ba78-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ba78-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1ba78-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ba78-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ba78-108">DESCRIPTION</span></span>
<span data-ttu-id="1ba78-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="1ba78-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="1ba78-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ba78-110">EXAMPLES</span></span>

### <span data-ttu-id="1ba78-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="1ba78-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="1ba78-112">Az összes eszköz kapcsolati karakterláncának megjelenítése egy Iot-központban.</span><span class="sxs-lookup"><span data-stu-id="1ba78-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="1ba78-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1ba78-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="1ba78-114">Egy IoT-eszköz másodlagos kapcsolati karakterláncának lekérte.</span><span class="sxs-lookup"><span data-stu-id="1ba78-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="1ba78-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ba78-115">PARAMETERS</span></span>

### <span data-ttu-id="1ba78-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba78-116">-DefaultProfile</span></span>
<span data-ttu-id="1ba78-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ba78-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ba78-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1ba78-118">-DeviceId</span></span>
<span data-ttu-id="1ba78-119">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1ba78-119">Target Device Id.</span></span>

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

### <span data-ttu-id="1ba78-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ba78-120">-InputObject</span></span>
<span data-ttu-id="1ba78-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="1ba78-121">IotHub object</span></span>

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

### <span data-ttu-id="1ba78-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1ba78-122">-IotHubName</span></span>
<span data-ttu-id="1ba78-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="1ba78-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1ba78-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1ba78-124">-KeyType</span></span>
<span data-ttu-id="1ba78-125">Hitelesítés megosztott hozzáférési házirendkulcstípusa.</span><span class="sxs-lookup"><span data-stu-id="1ba78-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba78-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ba78-126">-ResourceGroupName</span></span>
<span data-ttu-id="1ba78-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1ba78-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1ba78-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ba78-128">-ResourceId</span></span>
<span data-ttu-id="1ba78-129">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="1ba78-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1ba78-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba78-130">CommonParameters</span></span>
<span data-ttu-id="1ba78-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba78-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba78-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ba78-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba78-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ba78-133">INPUTS</span></span>

### <span data-ttu-id="1ba78-134">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1ba78-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1ba78-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1ba78-135">System.String</span></span>

## <span data-ttu-id="1ba78-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ba78-136">OUTPUTS</span></span>

### <span data-ttu-id="1ba78-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="1ba78-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="1ba78-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ba78-138">NOTES</span></span>

## <span data-ttu-id="1ba78-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ba78-139">RELATED LINKS</span></span>
