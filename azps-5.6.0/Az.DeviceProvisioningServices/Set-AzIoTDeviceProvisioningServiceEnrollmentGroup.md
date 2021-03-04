---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 511d0445f7c27acf7ace059852f6e4a8b23655b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935202"
---
# <span data-ttu-id="efb3c-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="efb3c-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="efb3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efb3c-102">SYNOPSIS</span></span>
<span data-ttu-id="efb3c-103">Eszközregisztrációs csoport frissítése.</span><span class="sxs-lookup"><span data-stu-id="efb3c-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="efb3c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="efb3c-104">SYNTAX</span></span>

### <span data-ttu-id="efb3c-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="efb3c-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efb3c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="efb3c-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efb3c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="efb3c-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efb3c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="efb3c-108">DESCRIPTION</span></span>
<span data-ttu-id="efb3c-109">Frissítsen egy regisztrációs csoportot egy Azure IoT-központ eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="efb3c-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="efb3c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="efb3c-110">EXAMPLES</span></span>

### <span data-ttu-id="efb3c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="efb3c-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="efb3c-112">Frissítse egy regisztrációs csoport kiosztási házirendját és központját.</span><span class="sxs-lookup"><span data-stu-id="efb3c-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="efb3c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="efb3c-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="efb3c-114">Frissítse egy regisztrációs csoport kezdeti állapotát.</span><span class="sxs-lookup"><span data-stu-id="efb3c-114">Update an enrollment group's initial twin state.</span></span>

### <span data-ttu-id="efb3c-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="efb3c-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -PrimaryKey "newPrimaryKey" -SecondaryKey "newSecondaryKey"
```

<span data-ttu-id="efb3c-116">Szimmetrikus regisztrációs csoport elsődleges és másodlagos kulcsának frissítése</span><span class="sxs-lookup"><span data-stu-id="efb3c-116">Update a symmetric key enrollment group's primary and secondary keys</span></span>

## <span data-ttu-id="efb3c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efb3c-117">PARAMETERS</span></span>

### <span data-ttu-id="efb3c-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="efb3c-118">-AllocationPolicy</span></span>
<span data-ttu-id="efb3c-119">A Központhoz rendelt eszköz kiosztásának típusa.</span><span class="sxs-lookup"><span data-stu-id="efb3c-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="efb3c-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="efb3c-120">-ApiVersion</span></span>
<span data-ttu-id="efb3c-121">A kiépítési szolgáltatás API-verziója az egyéni hozzárendelési kérésben.</span><span class="sxs-lookup"><span data-stu-id="efb3c-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="efb3c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb3c-122">-DefaultProfile</span></span>
<span data-ttu-id="efb3c-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efb3c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efb3c-124">-Kívánt</span><span class="sxs-lookup"><span data-stu-id="efb3c-124">-Desired</span></span>
<span data-ttu-id="efb3c-125">A kezdeti kíván tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="efb3c-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="efb3c-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="efb3c-126">-DpsName</span></span>
<span data-ttu-id="efb3c-127">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="efb3c-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="efb3c-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="efb3c-128">-DpsObject</span></span>
<span data-ttu-id="efb3c-129">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="efb3c-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="efb3c-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="efb3c-130">-EdgeEnabled</span></span>
<span data-ttu-id="efb3c-131">Flag indicating edge enablement.</span><span class="sxs-lookup"><span data-stu-id="efb3c-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="efb3c-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="efb3c-132">-IotHub</span></span>
<span data-ttu-id="efb3c-133">A cél IoT-központ állomásneve.</span><span class="sxs-lookup"><span data-stu-id="efb3c-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="efb3c-134">Több IoT-központhoz használjon térközt választó listát.</span><span class="sxs-lookup"><span data-stu-id="efb3c-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="efb3c-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="efb3c-135">-IotHubHostName</span></span>
<span data-ttu-id="efb3c-136">A cél IoT-központ állomásneve.</span><span class="sxs-lookup"><span data-stu-id="efb3c-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="efb3c-137">-Name</span><span class="sxs-lookup"><span data-stu-id="efb3c-137">-Name</span></span>
<span data-ttu-id="efb3c-138">A regisztrációs csoport neve.</span><span class="sxs-lookup"><span data-stu-id="efb3c-138">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="efb3c-139">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="efb3c-139">-PrimaryCAName</span></span>
<span data-ttu-id="efb3c-140">Az elsődleges legfelső szintű hitelesítésszolgáltatói tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="efb3c-140">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="efb3c-141">Ha a legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal való hitelesítést szeretné biztosítani, akkor meg kell adni egy legfelső szintű hitelesítésszolgáltató nevét.</span><span class="sxs-lookup"><span data-stu-id="efb3c-141">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="efb3c-142">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="efb3c-142">-PrimaryCertificate</span></span>
<span data-ttu-id="efb3c-143">Az elsődleges tanúsítványt tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="efb3c-143">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="efb3c-144">Az X509-es tanúsítvány .cer fájl vagy .pem fájl elérési útvonalának 64-es alapformátumú reprezentációja.</span><span class="sxs-lookup"><span data-stu-id="efb3c-144">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="efb3c-145">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="efb3c-145">-PrimaryKey</span></span>
<span data-ttu-id="efb3c-146">A base64 formátumban tárolt elsődleges szimmetrikus megosztott hozzáférési kulcs.</span><span class="sxs-lookup"><span data-stu-id="efb3c-146">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="efb3c-147">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="efb3c-147">-ProvisioningStatus</span></span>
<span data-ttu-id="efb3c-148">A regisztrációs bejegyzés engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="efb3c-148">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="efb3c-149">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="efb3c-149">-ReprovisionPolicy</span></span>
<span data-ttu-id="efb3c-150">A másik Iot-központba való újraépítéssel kezelni szükséges eszközadatok.</span><span class="sxs-lookup"><span data-stu-id="efb3c-150">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="efb3c-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efb3c-151">-ResourceGroupName</span></span>
<span data-ttu-id="efb3c-152">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="efb3c-152">Name of the Resource Group</span></span>

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

### <span data-ttu-id="efb3c-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efb3c-153">-ResourceId</span></span>
<span data-ttu-id="efb3c-154">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="efb3c-154">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="efb3c-155">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="efb3c-155">-RootCertificate</span></span>
<span data-ttu-id="efb3c-156">Főtanúsítványok használatával X509atte-tanúsítványt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="efb3c-156">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="efb3c-157">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="efb3c-157">-SecondaryCAName</span></span>
<span data-ttu-id="efb3c-158">A másodlagos legfelső szintű hitelesítésszolgáltatói tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="efb3c-158">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="efb3c-159">Ha a legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal való hitelesítést szeretné biztosítani, akkor meg kell adni egy legfelső szintű hitelesítésszolgáltató nevét.</span><span class="sxs-lookup"><span data-stu-id="efb3c-159">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="efb3c-160">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="efb3c-160">-SecondaryCertificate</span></span>
<span data-ttu-id="efb3c-161">A másodlagos tanúsítványt tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="efb3c-161">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="efb3c-162">Az X509-es tanúsítvány .cer fájl vagy .pem fájl elérési útvonalának 64-es alapformátumú reprezentációja.</span><span class="sxs-lookup"><span data-stu-id="efb3c-162">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="efb3c-163">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="efb3c-163">-SecondaryKey</span></span>
<span data-ttu-id="efb3c-164">A másodlagos szimmetrikus megosztott hozzáférési kulcs, amely base64 formátumban van tárolva.</span><span class="sxs-lookup"><span data-stu-id="efb3c-164">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="efb3c-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="efb3c-165">-Tag</span></span>
<span data-ttu-id="efb3c-166">Kezdeti címkecímkék.</span><span class="sxs-lookup"><span data-stu-id="efb3c-166">Initial twin tags.</span></span>

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

### <span data-ttu-id="efb3c-167">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="efb3c-167">-WebhookUrl</span></span>
<span data-ttu-id="efb3c-168">Az egyéni hozzárendelési kérések webhook URL-címe.</span><span class="sxs-lookup"><span data-stu-id="efb3c-168">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="efb3c-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efb3c-169">-Confirm</span></span>
<span data-ttu-id="efb3c-170">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="efb3c-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efb3c-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efb3c-171">-WhatIf</span></span>
<span data-ttu-id="efb3c-172">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="efb3c-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efb3c-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efb3c-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efb3c-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb3c-174">CommonParameters</span></span>
<span data-ttu-id="efb3c-175">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efb3c-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb3c-176">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efb3c-176">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb3c-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efb3c-177">INPUTS</span></span>

### <span data-ttu-id="efb3c-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="efb3c-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="efb3c-179">System.String</span><span class="sxs-lookup"><span data-stu-id="efb3c-179">System.String</span></span>

## <span data-ttu-id="efb3c-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efb3c-180">OUTPUTS</span></span>

### <span data-ttu-id="efb3c-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="efb3c-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="efb3c-182">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="efb3c-182">NOTES</span></span>

## <span data-ttu-id="efb3c-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efb3c-183">RELATED LINKS</span></span>
