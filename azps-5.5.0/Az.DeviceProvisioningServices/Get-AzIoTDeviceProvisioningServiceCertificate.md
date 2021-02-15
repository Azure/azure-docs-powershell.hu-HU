---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: aa51001163e4559dd0d3ef7edfb48abd3448c0b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204198"
---
# <span data-ttu-id="4699d-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="4699d-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="4699d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4699d-102">SYNOPSIS</span></span>
<span data-ttu-id="4699d-103">Az Azure IoT Hub eszköz kiépítési szolgáltatásában található összes tanúsítványt vagy adott tanúsítványt sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="4699d-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4699d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4699d-104">SYNTAX</span></span>

### <span data-ttu-id="4699d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4699d-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4699d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4699d-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4699d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4699d-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4699d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4699d-108">DESCRIPTION</span></span>
<span data-ttu-id="4699d-109">Az Azure IoT Hub eszköz kiépítési szolgáltatásában található hitelesítésszolgáltatói tanúsítványok részletes magyarázatát https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates lásd: .</span><span class="sxs-lookup"><span data-stu-id="4699d-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="4699d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4699d-110">EXAMPLES</span></span>

### <span data-ttu-id="4699d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4699d-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="4699d-112">Részletek megjelenítése a "mycertificate" szolgáltatásról egy Azure IoT Hub-eszköz kiépítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="4699d-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="4699d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4699d-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="4699d-114">List all certificates in "myiotdps" using pipeline.</span><span class="sxs-lookup"><span data-stu-id="4699d-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="4699d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4699d-115">PARAMETERS</span></span>

### <span data-ttu-id="4699d-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="4699d-116">-CertificateName</span></span>
<span data-ttu-id="4699d-117">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="4699d-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="4699d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4699d-118">-DefaultProfile</span></span>
<span data-ttu-id="4699d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4699d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4699d-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4699d-120">-DpsObject</span></span>
<span data-ttu-id="4699d-121">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="4699d-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4699d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4699d-122">-Name</span></span>
<span data-ttu-id="4699d-123">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="4699d-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4699d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4699d-124">-ResourceGroupName</span></span>
<span data-ttu-id="4699d-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4699d-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4699d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4699d-126">-ResourceId</span></span>
<span data-ttu-id="4699d-127">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4699d-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4699d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4699d-128">CommonParameters</span></span>
<span data-ttu-id="4699d-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4699d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4699d-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4699d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4699d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4699d-131">INPUTS</span></span>

### <span data-ttu-id="4699d-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4699d-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4699d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4699d-133">System.String</span></span>

## <span data-ttu-id="4699d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4699d-134">OUTPUTS</span></span>

### <span data-ttu-id="4699d-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="4699d-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="4699d-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4699d-136">NOTES</span></span>

## <span data-ttu-id="4699d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4699d-137">RELATED LINKS</span></span>
