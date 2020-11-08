---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185514"
---
# <span data-ttu-id="00880-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="00880-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="00880-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00880-102">SYNOPSIS</span></span>
<span data-ttu-id="00880-103">Megkapja az eszköz regisztrációs állapotát.</span><span class="sxs-lookup"><span data-stu-id="00880-103">Gets the device registration state.</span></span>

## <span data-ttu-id="00880-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00880-104">SYNTAX</span></span>

### <span data-ttu-id="00880-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00880-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00880-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="00880-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00880-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="00880-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00880-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="00880-108">DESCRIPTION</span></span>
<span data-ttu-id="00880-109">Az enrollmentGroup-ban az Azure IoT hub eszközök kiépítési szolgáltatása során az eszköz regisztrációs állapotát vagy a regisztrációs állapotot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="00880-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="00880-110">Példák</span><span class="sxs-lookup"><span data-stu-id="00880-110">EXAMPLES</span></span>

### <span data-ttu-id="00880-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="00880-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="00880-112">Az eszköz regisztrációs állapotával kapcsolatos adatok beszerzése az Azure IoT hub eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="00880-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="00880-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="00880-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="00880-114">Ebben a enrollmentGroup az eszközök összes regisztrációs állapotát felsorolhatja.</span><span class="sxs-lookup"><span data-stu-id="00880-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="00880-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00880-115">PARAMETERS</span></span>

### <span data-ttu-id="00880-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00880-116">-DefaultProfile</span></span>
<span data-ttu-id="00880-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00880-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00880-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="00880-118">-DpsName</span></span>
<span data-ttu-id="00880-119">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="00880-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="00880-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="00880-120">-DpsObject</span></span>
<span data-ttu-id="00880-121">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="00880-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00880-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="00880-122">-EnrollmentId</span></span>
<span data-ttu-id="00880-123">A beiratkozási csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00880-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="00880-124">-Query</span><span class="sxs-lookup"><span data-stu-id="00880-124">-Query</span></span>
<span data-ttu-id="00880-125">SQL-lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="00880-125">Sql query.</span></span>

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

### <span data-ttu-id="00880-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="00880-126">-RegistrationId</span></span>
<span data-ttu-id="00880-127">Az eszköz regisztrációjának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00880-127">ID of device registration.</span></span>

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

### <span data-ttu-id="00880-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00880-128">-ResourceGroupName</span></span>
<span data-ttu-id="00880-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="00880-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="00880-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00880-130">-ResourceId</span></span>
<span data-ttu-id="00880-131">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="00880-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="00880-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00880-132">CommonParameters</span></span>
<span data-ttu-id="00880-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00880-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00880-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00880-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00880-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00880-135">INPUTS</span></span>

### <span data-ttu-id="00880-136">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="00880-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="00880-137">System. String</span><span class="sxs-lookup"><span data-stu-id="00880-137">System.String</span></span>

## <span data-ttu-id="00880-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00880-138">OUTPUTS</span></span>

### <span data-ttu-id="00880-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="00880-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="00880-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates []</span><span class="sxs-lookup"><span data-stu-id="00880-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="00880-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00880-141">NOTES</span></span>

## <span data-ttu-id="00880-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00880-142">RELATED LINKS</span></span>
