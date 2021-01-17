---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467806"
---
# <span data-ttu-id="42c94-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="42c94-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="42c94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42c94-102">SYNOPSIS</span></span>
<span data-ttu-id="42c94-103">Az eszköz regisztrációs állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="42c94-103">Gets the device registration state.</span></span>

## <span data-ttu-id="42c94-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="42c94-104">SYNTAX</span></span>

### <span data-ttu-id="42c94-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="42c94-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42c94-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="42c94-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42c94-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="42c94-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42c94-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="42c94-108">DESCRIPTION</span></span>
<span data-ttu-id="42c94-109">Szerezze be az eszköz regisztrációs állapotát vagy az eszközök regisztrációs állapotát egy Azure IoT-központ eszközépítési szolgáltatásában a enrollmentGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="42c94-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="42c94-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="42c94-110">EXAMPLES</span></span>

### <span data-ttu-id="42c94-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="42c94-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="42c94-112">Szerezze be az eszköz regisztrációs állapotát egy Azure IoT Hub eszközépítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="42c94-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="42c94-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="42c94-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="42c94-114">List all the registration state of devices in this enrollmentGroup.</span><span class="sxs-lookup"><span data-stu-id="42c94-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="42c94-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42c94-115">PARAMETERS</span></span>

### <span data-ttu-id="42c94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c94-116">-DefaultProfile</span></span>
<span data-ttu-id="42c94-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42c94-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42c94-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="42c94-118">-DpsName</span></span>
<span data-ttu-id="42c94-119">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="42c94-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="42c94-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="42c94-120">-DpsObject</span></span>
<span data-ttu-id="42c94-121">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="42c94-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="42c94-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="42c94-122">-EnrollmentId</span></span>
<span data-ttu-id="42c94-123">A regisztrációs csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="42c94-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="42c94-124">-Query</span><span class="sxs-lookup"><span data-stu-id="42c94-124">-Query</span></span>
<span data-ttu-id="42c94-125">Sql-lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="42c94-125">Sql query.</span></span>

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

### <span data-ttu-id="42c94-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="42c94-126">-RegistrationId</span></span>
<span data-ttu-id="42c94-127">Az eszközregisztráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="42c94-127">ID of device registration.</span></span>

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

### <span data-ttu-id="42c94-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42c94-128">-ResourceGroupName</span></span>
<span data-ttu-id="42c94-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="42c94-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="42c94-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42c94-130">-ResourceId</span></span>
<span data-ttu-id="42c94-131">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="42c94-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="42c94-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c94-132">CommonParameters</span></span>
<span data-ttu-id="42c94-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42c94-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c94-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42c94-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c94-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42c94-135">INPUTS</span></span>

### <span data-ttu-id="42c94-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="42c94-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="42c94-137">System.String</span><span class="sxs-lookup"><span data-stu-id="42c94-137">System.String</span></span>

## <span data-ttu-id="42c94-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42c94-138">OUTPUTS</span></span>

### <span data-ttu-id="42c94-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="42c94-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="42c94-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span><span class="sxs-lookup"><span data-stu-id="42c94-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="42c94-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="42c94-141">NOTES</span></span>

## <span data-ttu-id="42c94-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42c94-142">RELATED LINKS</span></span>
