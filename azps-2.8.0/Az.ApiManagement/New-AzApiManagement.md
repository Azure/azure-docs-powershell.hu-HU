---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 489df2abd46f3ec198422991c2627804f6dc140b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668080"
---
# <span data-ttu-id="e4b53-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e4b53-101">New-AzApiManagement</span></span>

## <span data-ttu-id="e4b53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4b53-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b53-103">API-kezelési központi telepítőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e4b53-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="e4b53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4b53-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-AssignIdentity] [-EnableClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4b53-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4b53-105">DESCRIPTION</span></span>
<span data-ttu-id="e4b53-106">A **New-AzApiManagement** parancsmag API-menedzsmentet hoz létre az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="e4b53-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="e4b53-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4b53-107">EXAMPLES</span></span>

### <span data-ttu-id="e4b53-108">Példa 1: fejlesztői szintű API-kezelési szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="e4b53-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="e4b53-109">Ez a parancs létrehoz egy fejlesztői Tier API-kezelési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e4b53-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="e4b53-110">A parancs a szervezetet és a rendszergazdai címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4b53-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="e4b53-111">A parancs nem adja meg a *SKU* paramétert.</span><span class="sxs-lookup"><span data-stu-id="e4b53-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="e4b53-112">Ezért a parancsmag a fejlesztő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="e4b53-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="e4b53-113">2. példa: a standard Tier-szolgáltatás létrehozása három egységgel</span><span class="sxs-lookup"><span data-stu-id="e4b53-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="e4b53-114">Ez a parancs létrehoz egy szabványos Tier API-kezelési szolgáltatást, amely három egységből áll.</span><span class="sxs-lookup"><span data-stu-id="e4b53-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="e4b53-115">3. példa: a fogyasztási szint szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="e4b53-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -AssignIdentity -EnableClientCertificate

PublicIPAddresses                     :
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-North-Europe/providers/Microsoft.ApiManagement/service/consumptionskuservice
Name                                  : consumptionskuservice
Location                              : West Europe
Sku                                   : Consumption
Capacity                              : 0
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://consumptionskuservice.azure-api.net
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {consumptionskuservice.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity
EnableClientCertificate               : True
ResourceGroupName                     : Api-Default-North-Europe
```

<span data-ttu-id="e4b53-116">Ezzel a paranccsal létrehozhatja a fogyasztási réteg API-kezelési szolgáltatását a Nyugat-európai ügyfél-tanúsítvánnyal.</span><span class="sxs-lookup"><span data-stu-id="e4b53-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="e4b53-117">4. példa: API-kezelési szolgáltatás létrehozása külső virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="e4b53-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="e4b53-118">Ez a parancs létrehoz egy prémium szintű API-kezelési szolgáltatást egy Azure virtuális hálózati alhálózatban, amelynek külső átjáró végpontja a Nyugat-amerikai fő területtel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="e4b53-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="e4b53-119">Példa 5: API-kezelési szolgáltatás létrehozása egy belső virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="e4b53-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="e4b53-120">Ez a parancs létrehoz egy prémium szintű API-kezelési szolgáltatást egy Azure virtuális hálózati alhálózatban, amelynek belső elérésű átjárója van, és egy fő területe van a Nyugat-Amerikai Egyesült Államokban.</span><span class="sxs-lookup"><span data-stu-id="e4b53-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="e4b53-121">Példa 6: API-kezelési szolgáltatás létrehozása és a TLS 1,0 protokoll engedélyezése</span><span class="sxs-lookup"><span data-stu-id="e4b53-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
```powershell
PS C:\> $enableTls=@{"Tls10" = "True"}
PS C:\> $sslSetting = New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls
PS C:\> New-AzApiManagement -ResourceGroupName Api-Default-CentralUS -Name "testtlspowershell" -Sku Standard -Location "CentralUS" -Organization "Microsoft" -AdminEmail "bar@contoso.com" -SslSetting $sslSetting

PublicIPAddresses                     : {23.99.140.18}
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-CentralUS/providers/Microsoft.ApiManagement/service/testtlspowershell
Name                                  : testtlspowershell
Location                              : Central US
Sku                                   : Standard
Capacity                              : 1
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://testtlspowershell.azure-api.net
RuntimeRegionalUrl                    : https://testtlspowershell-centralus-01.regional.azure-api.net
PortalUrl                             : https://testtlspowershell.portal.azure-api.net
ManagementApiUrl                      : https://testtlspowershell.management.azure-api.net
ScmUrl                                : https://testtlspowershell.scm.azure-api.net
PublisherEmail                        : bar@contoso.com
OrganizationName                      : Microsoft
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {testtlspowershell.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : Api-Default-CentralUS
```

<span data-ttu-id="e4b53-122">Ez a parancs létrehoz egy szabványos SKU API-kezelési szolgáltatást, és lehetővé teszi a TLS 1,0 a frontend ügyfélprogramot az átjáró és a backend-ügyfél ApiManagement az ApiManagement átjáró és a backend között.</span><span class="sxs-lookup"><span data-stu-id="e4b53-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="e4b53-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4b53-123">PARAMETERS</span></span>

### <span data-ttu-id="e4b53-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="e4b53-124">-AdditionalRegions</span></span>
<span data-ttu-id="e4b53-125">Az Azure API-menedzsment további központi terjesztési területei</span><span class="sxs-lookup"><span data-stu-id="e4b53-125">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="e4b53-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="e4b53-126">-AdminEmail</span></span>
<span data-ttu-id="e4b53-127">A származó e-mail-címet adja meg az API-kezelési rendszer által küldött összes értesítéshez.</span><span class="sxs-lookup"><span data-stu-id="e4b53-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="e4b53-128">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e4b53-128">-AssignIdentity</span></span>
<span data-ttu-id="e4b53-129">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást a kiszolgálóhoz a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használatra.</span><span class="sxs-lookup"><span data-stu-id="e4b53-129">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="e4b53-130">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="e4b53-130">-Capacity</span></span>
<span data-ttu-id="e4b53-131">Az Azure API-kezelési szolgáltatás SKU-kapacitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4b53-131">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="e4b53-132">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="e4b53-132">The default is one (1).</span></span>

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

### <span data-ttu-id="e4b53-133">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4b53-133">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="e4b53-134">Egyéni állomásnevek-konfigurációk</span><span class="sxs-lookup"><span data-stu-id="e4b53-134">Custom hostname configurations.</span></span> <span data-ttu-id="e4b53-135">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="e4b53-135">Default value is $null.</span></span> <span data-ttu-id="e4b53-136">A tompított $null az alapértelmezett állomásnevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4b53-136">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="e4b53-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b53-137">-DefaultProfile</span></span>
<span data-ttu-id="e4b53-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4b53-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4b53-139">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e4b53-139">-EnableClientCertificate</span></span>
<span data-ttu-id="e4b53-140">A megjelölés csak a raktározási SKU ApiManagement szolgáltatáshoz használható.</span><span class="sxs-lookup"><span data-stu-id="e4b53-140">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="e4b53-141">Ezzel kényszeríti az ügyfél tanúsítványát az átjáróhoz való minden kérésben.</span><span class="sxs-lookup"><span data-stu-id="e4b53-141">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="e4b53-142">Ez azt is lehetővé teszi, hogy az átjáró házirendjében hitelesítse a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="e4b53-142">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="e4b53-143">-Hely</span><span class="sxs-lookup"><span data-stu-id="e4b53-143">-Location</span></span>
<span data-ttu-id="e4b53-144">Az API-kezelési szolgáltatás létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4b53-144">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="e4b53-145">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="e4b53-145">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="e4b53-146">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4b53-146">-Name</span></span>
<span data-ttu-id="e4b53-147">Az API-kezelés bevezetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4b53-147">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="e4b53-148">-Szervezet</span><span class="sxs-lookup"><span data-stu-id="e4b53-148">-Organization</span></span>
<span data-ttu-id="e4b53-149">A szervezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4b53-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="e4b53-150">Az API-kezelés ezt a címet használja a fejlesztői portálon az értesítő e-mailekben.</span><span class="sxs-lookup"><span data-stu-id="e4b53-150">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="e4b53-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4b53-151">-ResourceGroupName</span></span>
<span data-ttu-id="e4b53-152">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt a parancsmag létrehoz egy API-kezelési telepítőt.</span><span class="sxs-lookup"><span data-stu-id="e4b53-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="e4b53-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="e4b53-153">-Sku</span></span>
<span data-ttu-id="e4b53-154">Az API-kezelési szolgáltatás rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4b53-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="e4b53-155">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="e4b53-155">Valid values are:</span></span> 
- <span data-ttu-id="e4b53-156">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="e4b53-156">Developer</span></span> 
- <span data-ttu-id="e4b53-157">Standard</span><span class="sxs-lookup"><span data-stu-id="e4b53-157">Standard</span></span> 
- <span data-ttu-id="e4b53-158">Prémium: az alapértelmezett fejlesztő.</span><span class="sxs-lookup"><span data-stu-id="e4b53-158">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4b53-159">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="e4b53-159">-SslSetting</span></span>
<span data-ttu-id="e4b53-160">Az ApiManagement szolgáltatás SSL-beállítása.</span><span class="sxs-lookup"><span data-stu-id="e4b53-160">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="e4b53-161">Az alapértelmezett érték a $null</span><span class="sxs-lookup"><span data-stu-id="e4b53-161">Default value is $null</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4b53-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4b53-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="e4b53-163">A belső HITELESÍTÉSSZOLGÁLTATÓ által kiállított tanúsítványokat a szolgáltatásra kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="e4b53-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="e4b53-164">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="e4b53-164">Default value is $null.</span></span>

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

### <span data-ttu-id="e4b53-165">-Címke</span><span class="sxs-lookup"><span data-stu-id="e4b53-165">-Tag</span></span>
<span data-ttu-id="e4b53-166">Címkék szótár.</span><span class="sxs-lookup"><span data-stu-id="e4b53-166">Tags dictionary.</span></span>

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

### <span data-ttu-id="e4b53-167">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e4b53-167">-VirtualNetwork</span></span>
<span data-ttu-id="e4b53-168">Az Azure API felügyeleti központi verziójának virtuális hálózati konfigurációja</span><span class="sxs-lookup"><span data-stu-id="e4b53-168">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="e4b53-169">-VpnType</span><span class="sxs-lookup"><span data-stu-id="e4b53-169">-VpnType</span></span>
<span data-ttu-id="e4b53-170">Az ApiManagement-telepítő virtuális hálózati típusa.</span><span class="sxs-lookup"><span data-stu-id="e4b53-170">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="e4b53-171">Érvényes értékek</span><span class="sxs-lookup"><span data-stu-id="e4b53-171">Valid Values are</span></span> 
- <span data-ttu-id="e4b53-172">"None" (alapértelmezett érték)</span><span class="sxs-lookup"><span data-stu-id="e4b53-172">"None" (Default Value.</span></span> <span data-ttu-id="e4b53-173">A ApiManagement nem része a virtuális hálózatnak ")</span><span class="sxs-lookup"><span data-stu-id="e4b53-173">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="e4b53-174">"Külső" (ApiManagement-telepítés olyan virtuális hálózatban van beállítva, amelynek van internetes végpontja)</span><span class="sxs-lookup"><span data-stu-id="e4b53-174">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="e4b53-175">"Belső" (a ApiManagement-telepítés olyan virtuális hálózatban van beállítva, amelynek intranetes végpontja van)</span><span class="sxs-lookup"><span data-stu-id="e4b53-175">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="e4b53-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b53-176">CommonParameters</span></span>
<span data-ttu-id="e4b53-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4b53-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b53-178">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e4b53-178">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b53-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4b53-179">INPUTS</span></span>

### <span data-ttu-id="e4b53-180">System. String</span><span class="sxs-lookup"><span data-stu-id="e4b53-180">System.String</span></span>

### <span data-ttu-id="e4b53-181">System. null ' 1 [[Microsoft. Azure. commands. ApiManagement. models. PsApiManagementSku, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e4b53-181">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e4b53-182">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e4b53-182">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e4b53-183">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e4b53-183">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="e4b53-184">System. Collections. Generic. Dictionary ' 2 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e], [System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e4b53-184">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e4b53-185">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="e4b53-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="e4b53-186">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="e4b53-186">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="e4b53-187">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="e4b53-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="e4b53-188">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4b53-188">OUTPUTS</span></span>

### <span data-ttu-id="e4b53-189">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e4b53-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e4b53-190">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4b53-190">NOTES</span></span>

## <span data-ttu-id="e4b53-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4b53-191">RELATED LINKS</span></span>

[<span data-ttu-id="e4b53-192">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e4b53-192">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="e4b53-193">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e4b53-193">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="e4b53-194">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e4b53-194">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="e4b53-195">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e4b53-195">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="e4b53-196">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e4b53-196">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


