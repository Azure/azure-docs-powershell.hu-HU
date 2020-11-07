---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: ab7d28c80f87eaf0220ead80e2c7fd76d3d2483b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666589"
---
# <span data-ttu-id="2ac9e-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="2ac9e-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="2ac9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ac9e-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac9e-103">Az Azure IoT hub-eszközök kiépítési szolgáltatásában található összes tanúsítvány vagy egy bizonyos tanúsítvány felsorolása.</span><span class="sxs-lookup"><span data-stu-id="2ac9e-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="2ac9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ac9e-104">SYNTAX</span></span>

### <span data-ttu-id="2ac9e-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ac9e-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac9e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2ac9e-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac9e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2ac9e-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ac9e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ac9e-108">DESCRIPTION</span></span>
<span data-ttu-id="2ac9e-109">A CA-tanúsítványok részletes magyarázatát az Azure IoT hub Device kiépítési szolgáltatásban című témakörben találja https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="2ac9e-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="2ac9e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2ac9e-110">EXAMPLES</span></span>

### <span data-ttu-id="2ac9e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2ac9e-111">Example 1</span></span>
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

<span data-ttu-id="2ac9e-112">A "mycertificate" részleteinek megjelenítése az Azure IoT hub eszközök kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="2ac9e-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="2ac9e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2ac9e-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="2ac9e-114">Az összes tanúsítvány listázása a "myiotdps"-ban csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="2ac9e-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="2ac9e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ac9e-115">PARAMETERS</span></span>

### <span data-ttu-id="2ac9e-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2ac9e-116">-CertificateName</span></span>
<span data-ttu-id="2ac9e-117">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="2ac9e-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="2ac9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac9e-118">-DefaultProfile</span></span>
<span data-ttu-id="2ac9e-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ac9e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ac9e-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2ac9e-120">-DpsObject</span></span>
<span data-ttu-id="2ac9e-121">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="2ac9e-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2ac9e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ac9e-122">-Name</span></span>
<span data-ttu-id="2ac9e-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="2ac9e-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2ac9e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac9e-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ac9e-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2ac9e-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2ac9e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ac9e-126">-ResourceId</span></span>
<span data-ttu-id="2ac9e-127">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2ac9e-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2ac9e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac9e-128">CommonParameters</span></span>
<span data-ttu-id="2ac9e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ac9e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac9e-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac9e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac9e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ac9e-131">INPUTS</span></span>

### <span data-ttu-id="2ac9e-132">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2ac9e-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2ac9e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac9e-133">System.String</span></span>

## <span data-ttu-id="2ac9e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ac9e-134">OUTPUTS</span></span>

### <span data-ttu-id="2ac9e-135">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="2ac9e-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="2ac9e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ac9e-136">NOTES</span></span>

## <span data-ttu-id="2ac9e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ac9e-137">RELATED LINKS</span></span>
