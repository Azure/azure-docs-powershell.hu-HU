---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 79387b634bc42a4885139db35ad68a9145c02dba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009430"
---
# <span data-ttu-id="19483-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="19483-101">New-AzApiManagement</span></span>

## <span data-ttu-id="19483-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19483-102">SYNOPSIS</span></span>
<span data-ttu-id="19483-103">API-kezelési telepítést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="19483-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="19483-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19483-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-EnableClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19483-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19483-105">DESCRIPTION</span></span>
<span data-ttu-id="19483-106">A **New-AzApiManagement** parancsmag létrehoz egy API-kezelési telepítést az Azure API Managementben.</span><span class="sxs-lookup"><span data-stu-id="19483-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="19483-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19483-107">EXAMPLES</span></span>

### <span data-ttu-id="19483-108">1. példa: Fejlesztői szintű API-kezelő szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="19483-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS D:\> New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi2" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"


PublicIPAddresses                     : {104.43.240.65}
PrivateIPAddresses                    :
Id                                    : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/ContosoGroup02/providers/Microsoft.ApiManagement/service/ContosoApi2
Name                                  : ContosoApi2
Location                              : Central US
Sku                                   : Developer
Capacity                              : 1
CreatedTimeUtc                        : 2/24/2020 10:34:12 PM
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://contosoapi2.azure-api.net
RuntimeRegionalUrl                    : https://contosoapi2-centralus-01.regional.azure-api.net
PortalUrl                             : https://contosoapi2.portal.azure-api.net
DeveloperPortalUrl                    : https://contosoapi2.developer.azure-api.net
ManagementApiUrl                      : https://contosoapi2.management.azure-api.net
ScmUrl                                : https://contosoapi2.scm.azure-api.net
PublisherEmail                        : admin@contoso.com
OrganizationName                      : Contoso
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {contosoapi2.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : ContosoGroup02
```

<span data-ttu-id="19483-109">Ez a parancs fejlesztői szintű API-kezelő szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="19483-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="19483-110">A parancs megadja a szervezetet és a rendszergazda címét.</span><span class="sxs-lookup"><span data-stu-id="19483-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="19483-111">A parancs nem adja meg az *SKU paramétert.*</span><span class="sxs-lookup"><span data-stu-id="19483-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="19483-112">Ezért a parancsmag a Fejlesztőeszközök alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="19483-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="19483-113">2. példa: Standard szintű szolgáltatás létrehozása három egységből</span><span class="sxs-lookup"><span data-stu-id="19483-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="19483-114">Ez a parancs létrehoz egy standard szintű API-kezelő szolgáltatást, amely három egységből áll.</span><span class="sxs-lookup"><span data-stu-id="19483-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="19483-115">3. példa: Fogyasztási szint szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="19483-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -SystemAssignedIdentity -EnableClientCertificate

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

<span data-ttu-id="19483-116">Ez a parancs létrehoz egy felhasználásszintű API-kezelési szolgáltatást, amelynél engedélyezve van az ügyfél tanúsítványa Nyugat-Európában.</span><span class="sxs-lookup"><span data-stu-id="19483-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="19483-117">4. példa: API-kezelési szolgáltatás létrehozása külső virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="19483-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="19483-118">Ez a parancs egy prémium szintű API-kezelési szolgáltatást hoz létre egy Azure virtuális hálózati alhálózatban, amelynek külső átjáró végpontja van egy fő régióval az Egyesült Államok nyugati részén.</span><span class="sxs-lookup"><span data-stu-id="19483-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="19483-119">5. példa: API-kezelési szolgáltatás létrehozása belső virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="19483-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="19483-120">Ez a parancs egy prémiumszintű API-kezelési szolgáltatást hoz létre egy Azure virtuális hálózati alhálózatban, amelynek belső átjáró végpontja van egy fő régióval az Egyesült Államok nyugati részén.</span><span class="sxs-lookup"><span data-stu-id="19483-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="19483-121">6. példa: API-kezelési szolgáltatás létrehozása és TLS 1.0 protokoll engedélyezése</span><span class="sxs-lookup"><span data-stu-id="19483-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
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

<span data-ttu-id="19483-122">Ez a parancs létrehoz egy normál termékváltozat api-kezelési szolgáltatást, és engedélyezi a TLS 1.0-t az Előlapi ügyfélprogramban az ApiManagement Átjáró és a Backend ügyfélprogram között az ApiManagement átjáró és a Backend között.</span><span class="sxs-lookup"><span data-stu-id="19483-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="19483-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19483-123">PARAMETERS</span></span>

### <span data-ttu-id="19483-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="19483-124">-AdditionalRegions</span></span>
<span data-ttu-id="19483-125">Az Azure API-kezelés további telepítési régiói.</span><span class="sxs-lookup"><span data-stu-id="19483-125">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="19483-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="19483-126">-AdminEmail</span></span>
<span data-ttu-id="19483-127">Az API-kezelő rendszer által küldött összes értesítés eredeti e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19483-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="19483-128">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="19483-128">-Capacity</span></span>
<span data-ttu-id="19483-129">Az Azure API Felügyeleti szolgáltatás termékváltozat-kapacitását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="19483-129">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="19483-130">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="19483-130">The default is one (1).</span></span>

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

### <span data-ttu-id="19483-131">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="19483-131">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="19483-132">Egyéni állomásnév-konfigurációk.</span><span class="sxs-lookup"><span data-stu-id="19483-132">Custom hostname configurations.</span></span> <span data-ttu-id="19483-133">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="19483-133">Default value is $null.</span></span> <span data-ttu-id="19483-134">Ha $null adja meg az alapértelmezett állomásnevet.</span><span class="sxs-lookup"><span data-stu-id="19483-134">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="19483-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19483-135">-DefaultProfile</span></span>
<span data-ttu-id="19483-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19483-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19483-137">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="19483-137">-EnableClientCertificate</span></span>
<span data-ttu-id="19483-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span><span class="sxs-lookup"><span data-stu-id="19483-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="19483-139">Ez azt kényszeríti, hogy az ügyfél tanúsítványa minden, az átjárónak szóló kérésnél érvénybe lép.</span><span class="sxs-lookup"><span data-stu-id="19483-139">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="19483-140">Ez lehetővé teszi a tanúsítvány hitelesítését is az átjáró házirendjében.</span><span class="sxs-lookup"><span data-stu-id="19483-140">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="19483-141">-Location</span><span class="sxs-lookup"><span data-stu-id="19483-141">-Location</span></span>
<span data-ttu-id="19483-142">Megadja az Api Management szolgáltatás létrehozására használt helyet.</span><span class="sxs-lookup"><span data-stu-id="19483-142">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="19483-143">Érvényes helyek beszerzéséhez használja a Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | ahol {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="19483-143">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="19483-144">-Name</span><span class="sxs-lookup"><span data-stu-id="19483-144">-Name</span></span>
<span data-ttu-id="19483-145">Megadja az API-kezelés telepítésének nevét.</span><span class="sxs-lookup"><span data-stu-id="19483-145">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="19483-146">-Organization</span><span class="sxs-lookup"><span data-stu-id="19483-146">-Organization</span></span>
<span data-ttu-id="19483-147">A szervezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19483-147">Specifies the name of an organization.</span></span>
<span data-ttu-id="19483-148">Az API-kezelés ezt a címet használja a fejlesztői portálon az e-mail-értesítésekben.</span><span class="sxs-lookup"><span data-stu-id="19483-148">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="19483-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19483-149">-ResourceGroupName</span></span>
<span data-ttu-id="19483-150">Annak az erőforráscsoportnak a nevét adja meg, amely alatt ez a parancsmag API-kezelési telepítést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="19483-150">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="19483-151">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="19483-151">-Sku</span></span>
<span data-ttu-id="19483-152">Az API-kezelési szolgáltatás rétegét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="19483-152">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="19483-153">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="19483-153">Valid values are:</span></span> 
- <span data-ttu-id="19483-154">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="19483-154">Developer</span></span> 
- <span data-ttu-id="19483-155">Normál</span><span class="sxs-lookup"><span data-stu-id="19483-155">Standard</span></span> 
- <span data-ttu-id="19483-156">Premium Az alapértelmezett beállítás a Fejlesztőeszközök.</span><span class="sxs-lookup"><span data-stu-id="19483-156">Premium The default is Developer.</span></span>

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

### <span data-ttu-id="19483-157">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="19483-157">-SslSetting</span></span>
<span data-ttu-id="19483-158">Az ApiManagement szolgáltatás Ssl-beállítása.</span><span class="sxs-lookup"><span data-stu-id="19483-158">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="19483-159">Az alapértelmezett érték $null</span><span class="sxs-lookup"><span data-stu-id="19483-159">Default value is $null</span></span>

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

### <span data-ttu-id="19483-160">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="19483-160">-SystemAssignedIdentity</span></span>
<span data-ttu-id="19483-161">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a kiszolgálóhoz olyan kulcskezelő szolgáltatásokhoz, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="19483-161">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="19483-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="19483-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="19483-163">A szolgáltatásra telepítve a belső hitelesítésszolgáltató által kibocsátott tanúsítványok.</span><span class="sxs-lookup"><span data-stu-id="19483-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="19483-164">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="19483-164">Default value is $null.</span></span>

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

### <span data-ttu-id="19483-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="19483-165">-Tag</span></span>
<span data-ttu-id="19483-166">Címkék szótár.</span><span class="sxs-lookup"><span data-stu-id="19483-166">Tags dictionary.</span></span>

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

### <span data-ttu-id="19483-167">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="19483-167">-UserAssignedIdentity</span></span>
<span data-ttu-id="19483-168">Felhasználói identitásokat rendelhet ehhez a kiszolgálóhoz, hogy olyan kulcskezelő szolgáltatásokkal használja őket, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="19483-168">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19483-169">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19483-169">-VirtualNetwork</span></span>
<span data-ttu-id="19483-170">Virtual Network Configuration of master Azure API Management deployment region.</span><span class="sxs-lookup"><span data-stu-id="19483-170">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="19483-171">-VpnType</span><span class="sxs-lookup"><span data-stu-id="19483-171">-VpnType</span></span>
<span data-ttu-id="19483-172">Az ApiManagement-telepítés virtuális hálózattípusa.</span><span class="sxs-lookup"><span data-stu-id="19483-172">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="19483-173">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="19483-173">Valid Values are</span></span> 
- <span data-ttu-id="19483-174">"Nincs" (alapértelmezett érték.</span><span class="sxs-lookup"><span data-stu-id="19483-174">"None" (Default Value.</span></span> <span data-ttu-id="19483-175">Az ApiManagement nem része semmilyen virtuális hálózatnak")</span><span class="sxs-lookup"><span data-stu-id="19483-175">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="19483-176">"Külső" (Az ApiManagement-telepítés egy internetes végponttal rendelkező virtuális hálózaton belül van beállítva)</span><span class="sxs-lookup"><span data-stu-id="19483-176">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="19483-177">"Belső" (az ApiManagement-telepítés egy intranetes végponttal rendelkező virtuális hálózaton belül van beállítva)</span><span class="sxs-lookup"><span data-stu-id="19483-177">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="19483-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19483-178">CommonParameters</span></span>
<span data-ttu-id="19483-179">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19483-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19483-180">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19483-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19483-181">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19483-181">INPUTS</span></span>

### <span data-ttu-id="19483-182">System.String</span><span class="sxs-lookup"><span data-stu-id="19483-182">System.String</span></span>

### <span data-ttu-id="19483-183">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="19483-183">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="19483-184">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="19483-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="19483-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19483-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="19483-186">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="19483-186">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="19483-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span><span class="sxs-lookup"><span data-stu-id="19483-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="19483-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="19483-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="19483-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span><span class="sxs-lookup"><span data-stu-id="19483-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="19483-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19483-190">OUTPUTS</span></span>

### <span data-ttu-id="19483-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="19483-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="19483-192">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19483-192">NOTES</span></span>

## <span data-ttu-id="19483-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19483-193">RELATED LINKS</span></span>

[<span data-ttu-id="19483-194">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="19483-194">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="19483-195">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="19483-195">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="19483-196">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="19483-196">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="19483-197">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="19483-197">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="19483-198">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="19483-198">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


