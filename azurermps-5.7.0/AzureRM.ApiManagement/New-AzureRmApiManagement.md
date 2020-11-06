---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: ebf95d8e809731bdca2f288bc09054fd14353686
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503908"
---
# <span data-ttu-id="25dcc-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="25dcc-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="25dcc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="25dcc-103">API-kezelési központi telepítőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="25dcc-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25dcc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25dcc-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25dcc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="25dcc-105">DESCRIPTION</span></span>
<span data-ttu-id="25dcc-106">A **New-AzureRmApiManagement** parancsmag API-menedzsmentet hoz létre az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="25dcc-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="25dcc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="25dcc-107">EXAMPLES</span></span>

### <span data-ttu-id="25dcc-108">Példa 1: fejlesztői szintű API-kezelési szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="25dcc-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="25dcc-109">Ez a parancs létrehoz egy fejlesztői Tier API-kezelési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="25dcc-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="25dcc-110">A parancs a szervezetet és a rendszergazdai címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="25dcc-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="25dcc-111">A parancs nem adja meg a *SKU* paramétert.</span><span class="sxs-lookup"><span data-stu-id="25dcc-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="25dcc-112">Ezért a parancsmag a fejlesztő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="25dcc-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="25dcc-113">2. példa: a standard Tier-szolgáltatás létrehozása három egységgel</span><span class="sxs-lookup"><span data-stu-id="25dcc-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="25dcc-114">Ez a parancs létrehoz egy szabványos Tier API-kezelési szolgáltatást, amely három egységből áll.</span><span class="sxs-lookup"><span data-stu-id="25dcc-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="25dcc-115">3. példa: API-kezelési szolgáltatás létrehozása külső virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="25dcc-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="25dcc-116">Ez a parancs létrehoz egy prémium szintű API-kezelési szolgáltatást egy Azure virtuális hálózati alhálózatban, amelynek külső átjáró végpontja a Nyugat-amerikai fő területtel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="25dcc-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="25dcc-117">Példa 4: API-kezelési szolgáltatás létrehozása egy belső virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="25dcc-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="25dcc-118">Ez a parancs létrehoz egy prémium szintű API-kezelési szolgáltatást egy Azure virtuális hálózati alhálózatban, amelynek belső elérésű átjárója van, és egy fő területe van a Nyugat-Amerikai Egyesült Államokban.</span><span class="sxs-lookup"><span data-stu-id="25dcc-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="25dcc-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25dcc-119">PARAMETERS</span></span>

### <span data-ttu-id="25dcc-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="25dcc-120">-AdditionalRegions</span></span>
<span data-ttu-id="25dcc-121">Az Azure API-menedzsment további központi terjesztési területei</span><span class="sxs-lookup"><span data-stu-id="25dcc-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25dcc-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="25dcc-122">-AdminEmail</span></span>
<span data-ttu-id="25dcc-123">A származó e-mail-címet adja meg az API-kezelési rendszer által küldött összes értesítéshez.</span><span class="sxs-lookup"><span data-stu-id="25dcc-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25dcc-124">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="25dcc-124">-Capacity</span></span>
<span data-ttu-id="25dcc-125">Az Azure API-kezelési szolgáltatás SKU-kapacitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="25dcc-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="25dcc-126">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="25dcc-126">The default is one (1).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25dcc-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25dcc-127">-DefaultProfile</span></span>
<span data-ttu-id="25dcc-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25dcc-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25dcc-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="25dcc-129">-Location</span></span>
<span data-ttu-id="25dcc-130">Az API-kezelési szolgáltatás létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25dcc-130">Specifies the location to create the Api Management service.</span></span>

<span data-ttu-id="25dcc-131">Ha érvényes helyeket szeretne beolvasni, használja a "Microsoft. ApiManagement" ProviderNamespace Get-AzureRmResourceProvider parancsmagot. where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "szolgáltatás"} | Select-Object helyek</span><span class="sxs-lookup"><span data-stu-id="25dcc-131">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25dcc-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25dcc-132">-Name</span></span>
<span data-ttu-id="25dcc-133">Az API-kezelés bevezetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25dcc-133">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25dcc-134">-Szervezet</span><span class="sxs-lookup"><span data-stu-id="25dcc-134">-Organization</span></span>
<span data-ttu-id="25dcc-135">A szervezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25dcc-135">Specifies the name of an organization.</span></span>
<span data-ttu-id="25dcc-136">Az API-kezelés ezt a címet használja a fejlesztői portálon az értesítő e-mailekben.</span><span class="sxs-lookup"><span data-stu-id="25dcc-136">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25dcc-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25dcc-137">-ResourceGroupName</span></span>
<span data-ttu-id="25dcc-138">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt a parancsmag létrehoz egy API-kezelési telepítőt.</span><span class="sxs-lookup"><span data-stu-id="25dcc-138">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25dcc-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="25dcc-139">-Sku</span></span>
<span data-ttu-id="25dcc-140">Az API-kezelési szolgáltatás rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25dcc-140">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="25dcc-141">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="25dcc-141">Valid values are:</span></span> 

- <span data-ttu-id="25dcc-142">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="25dcc-142">Developer</span></span> 
- <span data-ttu-id="25dcc-143">Standard</span><span class="sxs-lookup"><span data-stu-id="25dcc-143">Standard</span></span> 
- <span data-ttu-id="25dcc-144">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="25dcc-144">Premium</span></span> 

<span data-ttu-id="25dcc-145">Az alapértelmezett a fejlesztő.</span><span class="sxs-lookup"><span data-stu-id="25dcc-145">The default is Developer.</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25dcc-146">-Címke</span><span class="sxs-lookup"><span data-stu-id="25dcc-146">-Tag</span></span>
<span data-ttu-id="25dcc-147">Címkék szótár.</span><span class="sxs-lookup"><span data-stu-id="25dcc-147">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25dcc-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="25dcc-148">-VirtualNetwork</span></span>
<span data-ttu-id="25dcc-149">Az Azure API felügyeleti központi verziójának virtuális hálózati konfigurációja</span><span class="sxs-lookup"><span data-stu-id="25dcc-149">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25dcc-150">-VpnType</span><span class="sxs-lookup"><span data-stu-id="25dcc-150">-VpnType</span></span>
<span data-ttu-id="25dcc-151">Az ApiManagement-telepítő virtuális hálózati típusa.</span><span class="sxs-lookup"><span data-stu-id="25dcc-151">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="25dcc-152">Érvényes értékek</span><span class="sxs-lookup"><span data-stu-id="25dcc-152">Valid Values are</span></span> 
- <span data-ttu-id="25dcc-153">"None" (alapértelmezett érték)</span><span class="sxs-lookup"><span data-stu-id="25dcc-153">"None" (Default Value.</span></span> <span data-ttu-id="25dcc-154">A ApiManagement nem része a virtuális hálózatnak ")</span><span class="sxs-lookup"><span data-stu-id="25dcc-154">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="25dcc-155">"Külső" (ApiManagement-telepítés olyan virtuális hálózatban van beállítva, amelynek van internetes végpontja)</span><span class="sxs-lookup"><span data-stu-id="25dcc-155">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="25dcc-156">"Belső" (a ApiManagement-telepítés olyan virtuális hálózatban van beállítva, amelynek intranetes végpontja van)</span><span class="sxs-lookup"><span data-stu-id="25dcc-156">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25dcc-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25dcc-157">CommonParameters</span></span>
<span data-ttu-id="25dcc-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25dcc-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25dcc-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25dcc-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25dcc-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25dcc-160">INPUTS</span></span>

### <span data-ttu-id="25dcc-161">Nincs</span><span class="sxs-lookup"><span data-stu-id="25dcc-161">None</span></span>
<span data-ttu-id="25dcc-162">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="25dcc-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25dcc-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25dcc-163">OUTPUTS</span></span>

### <span data-ttu-id="25dcc-164">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="25dcc-164">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="25dcc-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25dcc-165">NOTES</span></span>

## <span data-ttu-id="25dcc-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25dcc-166">RELATED LINKS</span></span>

[<span data-ttu-id="25dcc-167">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="25dcc-167">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="25dcc-168">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="25dcc-168">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="25dcc-169">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="25dcc-169">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="25dcc-170">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="25dcc-170">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


