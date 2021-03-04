---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 4087cb324f55d6445458fce2a8b79f5c39308b69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935209"
---
# <span data-ttu-id="3644a-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="3644a-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="3644a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3644a-102">SYNOPSIS</span></span>
<span data-ttu-id="3644a-103">Eszközregisztrációs rekord frissítése.</span><span class="sxs-lookup"><span data-stu-id="3644a-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="3644a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3644a-104">SYNTAX</span></span>

### <span data-ttu-id="3644a-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3644a-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3644a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3644a-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3644a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3644a-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3644a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3644a-108">DESCRIPTION</span></span>
<span data-ttu-id="3644a-109">Frissítsen egy eszköz regisztrálását egy Azure IoT Hub eszközépítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="3644a-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="3644a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3644a-110">EXAMPLES</span></span>

### <span data-ttu-id="3644a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="3644a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="3644a-112">Egy regisztrációs rekordhoz frissítse a foglalási házirendet és a központokat.</span><span class="sxs-lookup"><span data-stu-id="3644a-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="3644a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3644a-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="3644a-114">Frissítse a regisztráció kezdeti állapotát.</span><span class="sxs-lookup"><span data-stu-id="3644a-114">Update an enrollment's initial twin state.</span></span>

### <span data-ttu-id="3644a-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="3644a-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -PrimaryCertificate ".\primaryCertificate.cer" -SecondaryCertificate ".\secondaryCertificate.cer"
```

<span data-ttu-id="3644a-116">Szimmetrikus kulcs regisztrálása elsődleges és másodlagos tanúsítványának frissítése</span><span class="sxs-lookup"><span data-stu-id="3644a-116">Update a symmetric key enrollment's primary and secondary certificates</span></span>

## <span data-ttu-id="3644a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3644a-117">PARAMETERS</span></span>

### <span data-ttu-id="3644a-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="3644a-118">-AllocationPolicy</span></span>
<span data-ttu-id="3644a-119">A Központhoz rendelt eszköz kiosztásának típusa.</span><span class="sxs-lookup"><span data-stu-id="3644a-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="3644a-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3644a-120">-ApiVersion</span></span>
<span data-ttu-id="3644a-121">A kiépítési szolgáltatás API-verziója az egyéni hozzárendelési kérésben.</span><span class="sxs-lookup"><span data-stu-id="3644a-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="3644a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3644a-122">-DefaultProfile</span></span>
<span data-ttu-id="3644a-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3644a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3644a-124">-Kívánt</span><span class="sxs-lookup"><span data-stu-id="3644a-124">-Desired</span></span>
<span data-ttu-id="3644a-125">A kezdeti kíván tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="3644a-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="3644a-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="3644a-126">-DeviceId</span></span>
<span data-ttu-id="3644a-127">IoT-központ eszközazonosítója.</span><span class="sxs-lookup"><span data-stu-id="3644a-127">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="3644a-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="3644a-128">-DpsName</span></span>
<span data-ttu-id="3644a-129">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="3644a-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3644a-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="3644a-130">-DpsObject</span></span>
<span data-ttu-id="3644a-131">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="3644a-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="3644a-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="3644a-132">-EdgeEnabled</span></span>
<span data-ttu-id="3644a-133">Flag indicating edge enablement.</span><span class="sxs-lookup"><span data-stu-id="3644a-133">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3644a-134">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="3644a-134">-EndorsementKey</span></span>
<span data-ttu-id="3644a-135">TPM-támogató kulcs TPM-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="3644a-135">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="3644a-136">-IotHub</span><span class="sxs-lookup"><span data-stu-id="3644a-136">-IotHub</span></span>
<span data-ttu-id="3644a-137">A cél IoT-központ állomásneve.</span><span class="sxs-lookup"><span data-stu-id="3644a-137">Host name of target IoT Hub.</span></span>
<span data-ttu-id="3644a-138">Több IoT-központhoz használjon térközt választó listát.</span><span class="sxs-lookup"><span data-stu-id="3644a-138">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="3644a-139">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="3644a-139">-IotHubHostName</span></span>
<span data-ttu-id="3644a-140">A cél IoT-központ állomásneve.</span><span class="sxs-lookup"><span data-stu-id="3644a-140">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="3644a-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="3644a-141">-PrimaryCAName</span></span>
<span data-ttu-id="3644a-142">Az elsődleges legfelső szintű hitelesítésszolgáltatói tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="3644a-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="3644a-143">Ha a legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal való hitelesítést szeretné biztosítani, akkor meg kell adni egy legfelső szintű hitelesítésszolgáltató nevét.</span><span class="sxs-lookup"><span data-stu-id="3644a-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="3644a-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="3644a-144">-PrimaryCertificate</span></span>
<span data-ttu-id="3644a-145">Az elsődleges tanúsítványt tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="3644a-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="3644a-146">Az X509-es tanúsítvány .cer fájl vagy .pem fájl elérési útvonalának 64-es alapformátumú reprezentációja.</span><span class="sxs-lookup"><span data-stu-id="3644a-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="3644a-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="3644a-147">-PrimaryKey</span></span>
<span data-ttu-id="3644a-148">A base64 formátumban tárolt elsődleges szimmetrikus megosztott hozzáférési kulcs.</span><span class="sxs-lookup"><span data-stu-id="3644a-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="3644a-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="3644a-149">-ProvisioningStatus</span></span>
<span data-ttu-id="3644a-150">A regisztrációs bejegyzés engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="3644a-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="3644a-151">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="3644a-151">-RegistrationId</span></span>
<span data-ttu-id="3644a-152">Egyéni regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="3644a-152">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="3644a-153">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="3644a-153">-ReprovisionPolicy</span></span>
<span data-ttu-id="3644a-154">A másik Iot-központba való újraépítéssel kezelni szükséges eszközadatok.</span><span class="sxs-lookup"><span data-stu-id="3644a-154">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="3644a-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3644a-155">-ResourceGroupName</span></span>
<span data-ttu-id="3644a-156">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3644a-156">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3644a-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3644a-157">-ResourceId</span></span>
<span data-ttu-id="3644a-158">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3644a-158">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="3644a-159">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="3644a-159">-RootCertificate</span></span>
<span data-ttu-id="3644a-160">Váltás az X509attestation frissítésére főtanúsítványok használatával.</span><span class="sxs-lookup"><span data-stu-id="3644a-160">Switch to update X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="3644a-161">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="3644a-161">-SecondaryCAName</span></span>
<span data-ttu-id="3644a-162">A másodlagos legfelső szintű hitelesítésszolgáltatói tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="3644a-162">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="3644a-163">Ha a legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal való hitelesítést szeretné biztosítani, akkor meg kell adni egy legfelső szintű hitelesítésszolgáltató nevét.</span><span class="sxs-lookup"><span data-stu-id="3644a-163">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="3644a-164">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="3644a-164">-SecondaryCertificate</span></span>
<span data-ttu-id="3644a-165">A másodlagos tanúsítványt tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="3644a-165">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="3644a-166">Az X509-es tanúsítvány .cer fájl vagy .pem fájl elérési útvonalának 64-es alapformátumú reprezentációja.</span><span class="sxs-lookup"><span data-stu-id="3644a-166">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="3644a-167">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="3644a-167">-SecondaryKey</span></span>
<span data-ttu-id="3644a-168">A másodlagos szimmetrikus megosztott hozzáférési kulcs, amely base64 formátumban van tárolva.</span><span class="sxs-lookup"><span data-stu-id="3644a-168">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="3644a-169">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="3644a-169">-StorageRootKey</span></span>
<span data-ttu-id="3644a-170">TPM-eszköz TPM-tárterületének gyökérkulcsa.</span><span class="sxs-lookup"><span data-stu-id="3644a-170">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="3644a-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="3644a-171">-Tag</span></span>
<span data-ttu-id="3644a-172">Kezdeti címkecímkék.</span><span class="sxs-lookup"><span data-stu-id="3644a-172">Initial twin tags.</span></span>

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

### <span data-ttu-id="3644a-173">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="3644a-173">-WebhookUrl</span></span>
<span data-ttu-id="3644a-174">Az egyéni hozzárendelési kérések webhook URL-címe.</span><span class="sxs-lookup"><span data-stu-id="3644a-174">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="3644a-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3644a-175">-Confirm</span></span>
<span data-ttu-id="3644a-176">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3644a-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3644a-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3644a-177">-WhatIf</span></span>
<span data-ttu-id="3644a-178">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3644a-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3644a-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3644a-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3644a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3644a-180">CommonParameters</span></span>
<span data-ttu-id="3644a-181">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3644a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3644a-182">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3644a-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3644a-183">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3644a-183">INPUTS</span></span>

### <span data-ttu-id="3644a-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3644a-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="3644a-185">System.String</span><span class="sxs-lookup"><span data-stu-id="3644a-185">System.String</span></span>

## <span data-ttu-id="3644a-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3644a-186">OUTPUTS</span></span>

### <span data-ttu-id="3644a-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="3644a-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="3644a-188">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3644a-188">NOTES</span></span>

## <span data-ttu-id="3644a-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3644a-189">RELATED LINKS</span></span>
