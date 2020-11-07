---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 98e90b4c8275028ab3e62e7383505775271e8d09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672810"
---
# <span data-ttu-id="eb6b7-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6b7-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="eb6b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6b7-103">API-kezelési központi telepítőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb6b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb6b7-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb6b7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb6b7-105">DESCRIPTION</span></span>
<span data-ttu-id="eb6b7-106">A **New-AzureRmApiManagement** parancsmag API-menedzsmentet hoz létre az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="eb6b7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eb6b7-107">EXAMPLES</span></span>

### <span data-ttu-id="eb6b7-108">Példa 1: fejlesztői szintű API-kezelési szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="eb6b7-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="eb6b7-109">Ez a parancs létrehoz egy fejlesztői Tier API-kezelési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="eb6b7-110">A parancs a szervezetet és a rendszergazdai címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="eb6b7-111">A parancs nem adja meg a *SKU* paramétert.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="eb6b7-112">Ezért a parancsmag a fejlesztő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="eb6b7-113">2. példa: a standard Tier-szolgáltatás létrehozása három egységgel</span><span class="sxs-lookup"><span data-stu-id="eb6b7-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="eb6b7-114">Ez a parancs létrehoz egy szabványos Tier API-kezelési szolgáltatást, amely három egységből áll.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="eb6b7-115">3. példa: API-kezelési szolgáltatás létrehozása külső virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="eb6b7-115">Example 3: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="eb6b7-116">Ez a parancs létrehoz egy prémium szintű API-kezelési szolgáltatást egy Azure virtuális hálózati alhálózatban, amelynek külső átjáró végpontja a Nyugat-amerikai fő területtel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="eb6b7-117">Példa 4: API-kezelési szolgáltatás létrehozása egy belső virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="eb6b7-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="eb6b7-118">Ez a parancs létrehoz egy prémium szintű API-kezelési szolgáltatást egy Azure virtuális hálózati alhálózatban, amelynek belső elérésű átjárója van, és egy fő területe van a Nyugat-Amerikai Egyesült Államokban.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="eb6b7-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb6b7-119">PARAMETERS</span></span>

### <span data-ttu-id="eb6b7-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="eb6b7-120">-AdditionalRegions</span></span>
<span data-ttu-id="eb6b7-121">Az Azure API-menedzsment további központi terjesztési területei</span><span class="sxs-lookup"><span data-stu-id="eb6b7-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="eb6b7-122">-AdminEmail</span></span>
<span data-ttu-id="eb6b7-123">A származó e-mail-címet adja meg az API-kezelési rendszer által küldött összes értesítéshez.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="eb6b7-124">-AssignIdentity</span></span>
<span data-ttu-id="eb6b7-125">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást a kiszolgálóhoz a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használatra.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-125">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="eb6b7-126">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="eb6b7-126">-Capacity</span></span>
<span data-ttu-id="eb6b7-127">Az Azure API-kezelési szolgáltatás SKU-kapacitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-127">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="eb6b7-128">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="eb6b7-128">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-129">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb6b7-129">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="eb6b7-130">Egyéni állomásnevek-konfigurációk</span><span class="sxs-lookup"><span data-stu-id="eb6b7-130">Custom hostname configurations.</span></span> <span data-ttu-id="eb6b7-131">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-131">Default value is $null.</span></span> <span data-ttu-id="eb6b7-132">A tompított $null az alapértelmezett állomásnevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-132">Passing $null will set the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb6b7-133">-DefaultProfile</span></span>
<span data-ttu-id="eb6b7-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-135">-Hely</span><span class="sxs-lookup"><span data-stu-id="eb6b7-135">-Location</span></span>
<span data-ttu-id="eb6b7-136">Az API-kezelési szolgáltatás létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-136">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="eb6b7-137">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzureRmResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="eb6b7-137">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb6b7-138">-Name</span></span>
<span data-ttu-id="eb6b7-139">Az API-kezelés bevezetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-139">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-140">-Szervezet</span><span class="sxs-lookup"><span data-stu-id="eb6b7-140">-Organization</span></span>
<span data-ttu-id="eb6b7-141">A szervezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-141">Specifies the name of an organization.</span></span>
<span data-ttu-id="eb6b7-142">Az API-kezelés ezt a címet használja a fejlesztői portálon az értesítő e-mailekben.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-142">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb6b7-143">-ResourceGroupName</span></span>
<span data-ttu-id="eb6b7-144">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt a parancsmag létrehoz egy API-kezelési telepítőt.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-144">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-145">-SKU</span><span class="sxs-lookup"><span data-stu-id="eb6b7-145">-Sku</span></span>
<span data-ttu-id="eb6b7-146">Az API-kezelési szolgáltatás rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-146">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="eb6b7-147">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="eb6b7-147">Valid values are:</span></span> 
- <span data-ttu-id="eb6b7-148">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="eb6b7-148">Developer</span></span> 
- <span data-ttu-id="eb6b7-149">Standard</span><span class="sxs-lookup"><span data-stu-id="eb6b7-149">Standard</span></span> 
- <span data-ttu-id="eb6b7-150">Prémium: az alapértelmezett fejlesztő.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-150">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-151">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb6b7-151">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="eb6b7-152">A belső HITELESÍTÉSSZOLGÁLTATÓ által kiállított tanúsítványokat a szolgáltatásra kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-152">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="eb6b7-153">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-153">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-154">-Címke</span><span class="sxs-lookup"><span data-stu-id="eb6b7-154">-Tag</span></span>
<span data-ttu-id="eb6b7-155">Címkék szótár.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-155">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-156">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="eb6b7-156">-VirtualNetwork</span></span>
<span data-ttu-id="eb6b7-157">Az Azure API felügyeleti központi verziójának virtuális hálózati konfigurációja</span><span class="sxs-lookup"><span data-stu-id="eb6b7-157">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="eb6b7-158">-VpnType</span></span>
<span data-ttu-id="eb6b7-159">Az ApiManagement-telepítő virtuális hálózati típusa.</span><span class="sxs-lookup"><span data-stu-id="eb6b7-159">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="eb6b7-160">Érvényes értékek</span><span class="sxs-lookup"><span data-stu-id="eb6b7-160">Valid Values are</span></span> 
- <span data-ttu-id="eb6b7-161">"None" (alapértelmezett érték)</span><span class="sxs-lookup"><span data-stu-id="eb6b7-161">"None" (Default Value.</span></span> <span data-ttu-id="eb6b7-162">A ApiManagement nem része a virtuális hálózatnak ")</span><span class="sxs-lookup"><span data-stu-id="eb6b7-162">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="eb6b7-163">"Külső" (ApiManagement-telepítés olyan virtuális hálózatban van beállítva, amelynek van internetes végpontja)</span><span class="sxs-lookup"><span data-stu-id="eb6b7-163">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="eb6b7-164">"Belső" (a ApiManagement-telepítés olyan virtuális hálózatban van beállítva, amelynek intranetes végpontja van)</span><span class="sxs-lookup"><span data-stu-id="eb6b7-164">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b7-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6b7-165">CommonParameters</span></span>
<span data-ttu-id="eb6b7-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb6b7-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6b7-167">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb6b7-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6b7-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb6b7-168">INPUTS</span></span>

### <span data-ttu-id="eb6b7-169">System. String</span><span class="sxs-lookup"><span data-stu-id="eb6b7-169">System.String</span></span>

### <span data-ttu-id="eb6b7-170">System. null ' 1 [[Microsoft. Azure. commands. ApiManagement. models. PsApiManagementSku, Microsoft. Azure. commands. ApiManagement, Version = 6.1.2.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eb6b7-170">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eb6b7-171">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="eb6b7-171">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="eb6b7-172">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="eb6b7-172">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="eb6b7-173">System. Collections. Generic. Dictionary ' 2 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089], [System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="eb6b7-173">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="eb6b7-174">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="eb6b7-174">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="eb6b7-175">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="eb6b7-175">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="eb6b7-176">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="eb6b7-176">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="eb6b7-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb6b7-177">OUTPUTS</span></span>

### <span data-ttu-id="eb6b7-178">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6b7-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="eb6b7-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb6b7-179">NOTES</span></span>

## <span data-ttu-id="eb6b7-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb6b7-180">RELATED LINKS</span></span>

[<span data-ttu-id="eb6b7-181">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6b7-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="eb6b7-182">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6b7-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="eb6b7-183">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6b7-183">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)

[<span data-ttu-id="eb6b7-184">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6b7-184">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="eb6b7-185">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6b7-185">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


