---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328744"
---
# <span data-ttu-id="2054f-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="2054f-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="2054f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2054f-102">SYNOPSIS</span></span>
<span data-ttu-id="2054f-103">Az eszköz regisztrációs állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2054f-103">Gets the device registration state.</span></span>

## <span data-ttu-id="2054f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2054f-104">SYNTAX</span></span>

### <span data-ttu-id="2054f-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2054f-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2054f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2054f-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2054f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2054f-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2054f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2054f-108">DESCRIPTION</span></span>
<span data-ttu-id="2054f-109">Szerezze be az eszköz regisztrációs állapotát vagy az eszközök regisztrációs állapotát egy Azure IoT-központ eszközépítési szolgáltatásában a enrollmentGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="2054f-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="2054f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2054f-110">EXAMPLES</span></span>

### <span data-ttu-id="2054f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2054f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="2054f-112">Szerezze be az eszköz regisztrációs állapotát egy Azure IoT Hub eszközépítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="2054f-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="2054f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2054f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="2054f-114">List all the registration state of devices in this enrollmentGroup.</span><span class="sxs-lookup"><span data-stu-id="2054f-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="2054f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2054f-115">PARAMETERS</span></span>

### <span data-ttu-id="2054f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2054f-116">-DefaultProfile</span></span>
<span data-ttu-id="2054f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2054f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2054f-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="2054f-118">-DpsName</span></span>
<span data-ttu-id="2054f-119">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="2054f-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2054f-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2054f-120">-DpsObject</span></span>
<span data-ttu-id="2054f-121">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="2054f-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2054f-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="2054f-122">-EnrollmentId</span></span>
<span data-ttu-id="2054f-123">A regisztrációs csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2054f-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="2054f-124">-Query</span><span class="sxs-lookup"><span data-stu-id="2054f-124">-Query</span></span>
<span data-ttu-id="2054f-125">Sql-lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="2054f-125">Sql query.</span></span>

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

### <span data-ttu-id="2054f-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="2054f-126">-RegistrationId</span></span>
<span data-ttu-id="2054f-127">Az eszközregisztráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2054f-127">ID of device registration.</span></span>

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

### <span data-ttu-id="2054f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2054f-128">-ResourceGroupName</span></span>
<span data-ttu-id="2054f-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2054f-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2054f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2054f-130">-ResourceId</span></span>
<span data-ttu-id="2054f-131">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2054f-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2054f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2054f-132">CommonParameters</span></span>
<span data-ttu-id="2054f-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2054f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2054f-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2054f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2054f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2054f-135">INPUTS</span></span>

### <span data-ttu-id="2054f-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2054f-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2054f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2054f-137">System.String</span></span>

## <span data-ttu-id="2054f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2054f-138">OUTPUTS</span></span>

### <span data-ttu-id="2054f-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="2054f-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="2054f-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span><span class="sxs-lookup"><span data-stu-id="2054f-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="2054f-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2054f-141">NOTES</span></span>

## <span data-ttu-id="2054f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2054f-142">RELATED LINKS</span></span>
