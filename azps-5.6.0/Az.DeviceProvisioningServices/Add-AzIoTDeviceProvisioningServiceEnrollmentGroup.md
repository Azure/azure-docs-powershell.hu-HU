---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 89a1bede6ff90b58b83a7c401860c66430958fcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941841"
---
# <span data-ttu-id="a18be-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="a18be-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="a18be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a18be-102">SYNOPSIS</span></span>
<span data-ttu-id="a18be-103">Eszközregisztrációs csoport létrehozása.</span><span class="sxs-lookup"><span data-stu-id="a18be-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="a18be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a18be-104">SYNTAX</span></span>

### <span data-ttu-id="a18be-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a18be-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a18be-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a18be-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a18be-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a18be-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a18be-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a18be-108">DESCRIPTION</span></span>
<span data-ttu-id="a18be-109">Hozzon létre egy regisztrációs csoportot egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="a18be-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="a18be-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a18be-110">EXAMPLES</span></span>

### <span data-ttu-id="a18be-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a18be-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="a18be-112">Regisztráció létrehozása Szimmetrikus kulcs tanúsítványtípussal</span><span class="sxs-lookup"><span data-stu-id="a18be-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="a18be-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a18be-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="a18be-114">Regisztráció létrehozása X509-es tanúsítványtípussal</span><span class="sxs-lookup"><span data-stu-id="a18be-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="a18be-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="a18be-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="a18be-116">Hozzon létre egy regisztrációt Szimmetrikuskulcs típusú és kezdeti beállításállapotú tanúsítványokkal.</span><span class="sxs-lookup"><span data-stu-id="a18be-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="a18be-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a18be-117">PARAMETERS</span></span>

### <span data-ttu-id="a18be-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="a18be-118">-AllocationPolicy</span></span>
<span data-ttu-id="a18be-119">A Központhoz rendelt eszköz kiosztásának típusa.</span><span class="sxs-lookup"><span data-stu-id="a18be-119">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18be-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a18be-120">-ApiVersion</span></span>
<span data-ttu-id="a18be-121">A kiépítési szolgáltatás API-verziója az egyéni hozzárendelési kérésben.</span><span class="sxs-lookup"><span data-stu-id="a18be-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="a18be-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="a18be-122">-AttestationType</span></span>
<span data-ttu-id="a18be-123">Igazolási mechanizmus.</span><span class="sxs-lookup"><span data-stu-id="a18be-123">Attestation Mechanism.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAttestationMechanismType
Parameter Sets: (All)
Aliases:
Accepted values: None, Tpm, X509, SymmetricKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18be-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18be-124">-DefaultProfile</span></span>
<span data-ttu-id="a18be-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a18be-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a18be-126">-Kívánt</span><span class="sxs-lookup"><span data-stu-id="a18be-126">-Desired</span></span>
<span data-ttu-id="a18be-127">A kezdeti kíván tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="a18be-127">Initial twin desired properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18be-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="a18be-128">-DpsName</span></span>
<span data-ttu-id="a18be-129">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="a18be-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a18be-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a18be-130">-DpsObject</span></span>
<span data-ttu-id="a18be-131">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="a18be-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a18be-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="a18be-132">-EdgeEnabled</span></span>
<span data-ttu-id="a18be-133">Flag indicating edge enablement.</span><span class="sxs-lookup"><span data-stu-id="a18be-133">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18be-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="a18be-134">-IotHub</span></span>
<span data-ttu-id="a18be-135">A cél IoT-központ állomásneve.</span><span class="sxs-lookup"><span data-stu-id="a18be-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="a18be-136">Több IoT-központhoz használjon térközt választó listát.</span><span class="sxs-lookup"><span data-stu-id="a18be-136">Use space-separated list for multiple IoT Hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18be-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="a18be-137">-IotHubHostName</span></span>
<span data-ttu-id="a18be-138">A cél IoT-központ állomásneve.</span><span class="sxs-lookup"><span data-stu-id="a18be-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="a18be-139">-Name</span><span class="sxs-lookup"><span data-stu-id="a18be-139">-Name</span></span>
<span data-ttu-id="a18be-140">A regisztrációs csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a18be-140">Name of the enrollment group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18be-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="a18be-141">-PrimaryCAName</span></span>
<span data-ttu-id="a18be-142">Az elsődleges legfelső szintű hitelesítésszolgáltatói tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="a18be-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="a18be-143">Ha a legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal való hitelesítést szeretné biztosítani, akkor meg kell adni egy legfelső szintű hitelesítésszolgáltató nevét.</span><span class="sxs-lookup"><span data-stu-id="a18be-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="a18be-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="a18be-144">-PrimaryCertificate</span></span>
<span data-ttu-id="a18be-145">Az elsődleges tanúsítványt tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="a18be-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="a18be-146">Az X509-es tanúsítvány .cer fájl vagy .pem fájl elérési útvonalának 64-es alapformátumú reprezentációja.</span><span class="sxs-lookup"><span data-stu-id="a18be-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="a18be-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a18be-147">-PrimaryKey</span></span>
<span data-ttu-id="a18be-148">A base64 formátumban tárolt elsődleges szimmetrikus megosztott hozzáférési kulcs.</span><span class="sxs-lookup"><span data-stu-id="a18be-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="a18be-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="a18be-149">-ProvisioningStatus</span></span>
<span data-ttu-id="a18be-150">A regisztrációs bejegyzés engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="a18be-150">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18be-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="a18be-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="a18be-152">A másik Iot-központba való újraépítéssel kezelni szükséges eszközadatok.</span><span class="sxs-lookup"><span data-stu-id="a18be-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18be-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a18be-153">-ResourceGroupName</span></span>
<span data-ttu-id="a18be-154">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a18be-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a18be-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a18be-155">-ResourceId</span></span>
<span data-ttu-id="a18be-156">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a18be-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a18be-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="a18be-157">-RootCertificate</span></span>
<span data-ttu-id="a18be-158">Főtanúsítványok használatával X509atte-tanúsítványt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="a18be-158">Allows to create X509attestation using root certificates.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18be-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="a18be-159">-SecondaryCAName</span></span>
<span data-ttu-id="a18be-160">A másodlagos legfelső szintű hitelesítésszolgáltatói tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="a18be-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="a18be-161">Ha a legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal való hitelesítést szeretné biztosítani, akkor meg kell adni egy legfelső szintű hitelesítésszolgáltató nevét.</span><span class="sxs-lookup"><span data-stu-id="a18be-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="a18be-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="a18be-162">-SecondaryCertificate</span></span>
<span data-ttu-id="a18be-163">A másodlagos tanúsítványt tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="a18be-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="a18be-164">Az X509-es tanúsítvány .cer fájl vagy .pem fájl elérési útvonalának 64-es alapformátumú reprezentációja.</span><span class="sxs-lookup"><span data-stu-id="a18be-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="a18be-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="a18be-165">-SecondaryKey</span></span>
<span data-ttu-id="a18be-166">A másodlagos szimmetrikus megosztott hozzáférési kulcs, amely base64 formátumban van tárolva.</span><span class="sxs-lookup"><span data-stu-id="a18be-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="a18be-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="a18be-167">-Tag</span></span>
<span data-ttu-id="a18be-168">Kezdeti címkecímkék.</span><span class="sxs-lookup"><span data-stu-id="a18be-168">Initial twin tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18be-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="a18be-169">-WebhookUrl</span></span>
<span data-ttu-id="a18be-170">Az egyéni hozzárendelési kérések webhook URL-címe.</span><span class="sxs-lookup"><span data-stu-id="a18be-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="a18be-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a18be-171">-Confirm</span></span>
<span data-ttu-id="a18be-172">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a18be-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a18be-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a18be-173">-WhatIf</span></span>
<span data-ttu-id="a18be-174">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a18be-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a18be-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a18be-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a18be-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18be-176">CommonParameters</span></span>
<span data-ttu-id="a18be-177">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a18be-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18be-178">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a18be-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18be-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a18be-179">INPUTS</span></span>

### <span data-ttu-id="a18be-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a18be-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="a18be-181">System.String</span><span class="sxs-lookup"><span data-stu-id="a18be-181">System.String</span></span>

## <span data-ttu-id="a18be-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a18be-182">OUTPUTS</span></span>

### <span data-ttu-id="a18be-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="a18be-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="a18be-184">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a18be-184">NOTES</span></span>

## <span data-ttu-id="a18be-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a18be-185">RELATED LINKS</span></span>
