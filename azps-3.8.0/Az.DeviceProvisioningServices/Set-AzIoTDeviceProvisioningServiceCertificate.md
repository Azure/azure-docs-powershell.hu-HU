---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 9b995a0ed80bf32b770fe6b157a283534d01f743
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011908"
---
# <span data-ttu-id="0aa82-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="0aa82-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="0aa82-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0aa82-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa82-103">Ellenőrizzen egy Azure IoT hub-eszköz kiépítési szolgáltatási tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="0aa82-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="0aa82-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0aa82-104">SYNTAX</span></span>

### <span data-ttu-id="0aa82-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0aa82-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa82-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0aa82-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa82-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0aa82-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aa82-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0aa82-108">DESCRIPTION</span></span>
<span data-ttu-id="0aa82-109">Tanúsítvány ellenőrzéséhez a Generate-ellenőrzés-kód hívásával kapott ellenőrzési kódot tartalmazó ellenőrző tanúsítvány feltöltésével.</span><span class="sxs-lookup"><span data-stu-id="0aa82-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="0aa82-110">Ez az utolsó lépés a birtoklási folyamat igazolásakor.</span><span class="sxs-lookup"><span data-stu-id="0aa82-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="0aa82-111">Az Azure IoT hub eszköz kiépítési szolgáltatásának HITELESÍTÉSSZOLGÁLTATÓI tanúsítványainak részletes ismertetése a következő témakörben található: https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="0aa82-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="0aa82-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0aa82-112">EXAMPLES</span></span>

### <span data-ttu-id="0aa82-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0aa82-113">Example 1</span></span>
```
PS C:\> Set-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="0aa82-114">Ellenőrizze a "mycertificate" titkos kulcs tulajdonjogát.</span><span class="sxs-lookup"><span data-stu-id="0aa82-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="0aa82-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="0aa82-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | Set-AzIoTDpsCertificate -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="0aa82-116">Ellenőrizze a "mycertificate" privát kulcs tulajdonjogát a pipeline használatával.</span><span class="sxs-lookup"><span data-stu-id="0aa82-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="0aa82-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0aa82-117">PARAMETERS</span></span>

### <span data-ttu-id="0aa82-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="0aa82-118">-CertificateName</span></span>
<span data-ttu-id="0aa82-119">A IOT-eszköz kiépítési szolgáltatási tanúsítványának neve</span><span class="sxs-lookup"><span data-stu-id="0aa82-119">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa82-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa82-120">-DefaultProfile</span></span>
<span data-ttu-id="0aa82-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0aa82-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aa82-122">-ETAG</span><span class="sxs-lookup"><span data-stu-id="0aa82-122">-Etag</span></span>
<span data-ttu-id="0aa82-123">A tanúsítvány ETAG</span><span class="sxs-lookup"><span data-stu-id="0aa82-123">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa82-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aa82-124">-InputObject</span></span>
<span data-ttu-id="0aa82-125">IoT-eszköz kiépítési szolgáltatási tanúsítvány objektuma</span><span class="sxs-lookup"><span data-stu-id="0aa82-125">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0aa82-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0aa82-126">-Name</span></span>
<span data-ttu-id="0aa82-127">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="0aa82-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0aa82-128">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="0aa82-128">-Path</span></span>
<span data-ttu-id="0aa82-129">a X509. cer fájl vagy a. PEM fájl elérési útjának a 64-alapú megjelenítése</span><span class="sxs-lookup"><span data-stu-id="0aa82-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa82-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aa82-130">-ResourceGroupName</span></span>
<span data-ttu-id="0aa82-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0aa82-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0aa82-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0aa82-132">-ResourceId</span></span>
<span data-ttu-id="0aa82-133">IoT eszköz kiépítési szolgáltatási tanúsítvány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="0aa82-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="0aa82-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0aa82-134">-Confirm</span></span>
<span data-ttu-id="0aa82-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0aa82-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa82-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa82-136">-WhatIf</span></span>
<span data-ttu-id="0aa82-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0aa82-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aa82-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0aa82-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa82-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa82-139">CommonParameters</span></span>
<span data-ttu-id="0aa82-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0aa82-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa82-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aa82-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa82-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0aa82-142">INPUTS</span></span>

### <span data-ttu-id="0aa82-143">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="0aa82-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="0aa82-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0aa82-144">System.String</span></span>

## <span data-ttu-id="0aa82-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0aa82-145">OUTPUTS</span></span>

### <span data-ttu-id="0aa82-146">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="0aa82-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="0aa82-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0aa82-147">NOTES</span></span>

## <span data-ttu-id="0aa82-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0aa82-148">RELATED LINKS</span></span>
