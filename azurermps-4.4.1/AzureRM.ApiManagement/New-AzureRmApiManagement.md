---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 82e09e146999ce0bd320ba398ab2f196f1115688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498087"
---
# <span data-ttu-id="bd51c-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="bd51c-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="bd51c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd51c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd51c-103">API-kezelési központi telepítőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bd51c-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd51c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd51c-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd51c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd51c-105">DESCRIPTION</span></span>
<span data-ttu-id="bd51c-106">A **New-AzureRmApiManagement** parancsmag API-menedzsmentet hoz létre az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="bd51c-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="bd51c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bd51c-107">EXAMPLES</span></span>

### <span data-ttu-id="bd51c-108">Példa 1: fejlesztői szintű API-kezelési szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="bd51c-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="bd51c-109">Ez a parancs létrehoz egy fejlesztői Tier API-kezelési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="bd51c-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="bd51c-110">A parancs a szervezetet és a rendszergazdai címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd51c-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="bd51c-111">A parancs nem adja meg a *SKU* paramétert.</span><span class="sxs-lookup"><span data-stu-id="bd51c-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="bd51c-112">Ezért a parancsmag a fejlesztő alapértelmezett értékét használja.</span><span class="sxs-lookup"><span data-stu-id="bd51c-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="bd51c-113">2. példa: a standard Tier-szolgáltatás létrehozása három egységgel</span><span class="sxs-lookup"><span data-stu-id="bd51c-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="bd51c-114">Ez a parancs létrehoz egy szabványos Tier API-kezelési szolgáltatást, amely három egységből áll.</span><span class="sxs-lookup"><span data-stu-id="bd51c-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="bd51c-115">3. példa: API-kezelési szolgáltatás létrehozása külső virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="bd51c-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="bd51c-116">Ez a parancs létrehoz egy prémium szintű API-kezelési szolgáltatást egy Azure virtuális hálózati alhálózatban, amelynek külső átjáró végpontja a Nyugat-amerikai fő területtel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="bd51c-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="bd51c-117">Példa 4: API-kezelési szolgáltatás létrehozása egy belső virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="bd51c-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="bd51c-118">Ez a parancs létrehoz egy prémium szintű API-kezelési szolgáltatást egy Azure virtuális hálózati alhálózatban, amelynek belső elérésű átjárója van, és egy fő területe van a Nyugat-Amerikai Egyesült Államokban.</span><span class="sxs-lookup"><span data-stu-id="bd51c-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="bd51c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd51c-119">PARAMETERS</span></span>

### <span data-ttu-id="bd51c-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="bd51c-120">-AdditionalRegions</span></span>
<span data-ttu-id="bd51c-121">Az Azure API-menedzsment további központi terjesztési területei</span><span class="sxs-lookup"><span data-stu-id="bd51c-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="bd51c-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="bd51c-122">-AdminEmail</span></span>
<span data-ttu-id="bd51c-123">A származó e-mail-címet adja meg az API-kezelési rendszer által küldött összes értesítéshez.</span><span class="sxs-lookup"><span data-stu-id="bd51c-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="bd51c-124">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="bd51c-124">-Capacity</span></span>
<span data-ttu-id="bd51c-125">Az Azure API-kezelési szolgáltatás SKU-kapacitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd51c-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="bd51c-126">Az alapértelmezett érték egy (1).</span><span class="sxs-lookup"><span data-stu-id="bd51c-126">The default is one (1).</span></span>

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

### <span data-ttu-id="bd51c-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="bd51c-127">-Location</span></span>
<span data-ttu-id="bd51c-128">Azt a helyet adja meg, ahol ez a parancsmag API-kezelési központi telepítőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bd51c-128">Specifies the location in which this cmdlet creates an API Management deployment.</span></span>
<span data-ttu-id="bd51c-129">Ha érvényes helyeket szeretne beolvasni, használja az Get-AzureLocation parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bd51c-129">To obtain valid locations, use the Get-AzureLocation cmdlets.</span></span>

<span data-ttu-id="bd51c-130">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="bd51c-130">Valid values are:</span></span> 

- <span data-ttu-id="bd51c-131">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="bd51c-131">North Central US</span></span>
- <span data-ttu-id="bd51c-132">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="bd51c-132">South Central US</span></span>
- <span data-ttu-id="bd51c-133">Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="bd51c-133">Central US</span></span>
- <span data-ttu-id="bd51c-134">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="bd51c-134">West Europe</span></span>
- <span data-ttu-id="bd51c-135">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="bd51c-135">North Europe</span></span>
- <span data-ttu-id="bd51c-136">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="bd51c-136">West US</span></span>
- <span data-ttu-id="bd51c-137">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="bd51c-137">East US</span></span>
- <span data-ttu-id="bd51c-138">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="bd51c-138">East US 2</span></span>
- <span data-ttu-id="bd51c-139">Japán (kelet)</span><span class="sxs-lookup"><span data-stu-id="bd51c-139">Japan East</span></span>
- <span data-ttu-id="bd51c-140">Japán West</span><span class="sxs-lookup"><span data-stu-id="bd51c-140">Japan West</span></span>
- <span data-ttu-id="bd51c-141">Dél-Brazília</span><span class="sxs-lookup"><span data-stu-id="bd51c-141">Brazil South</span></span>
- <span data-ttu-id="bd51c-142">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="bd51c-142">Southeast Asia</span></span>
- <span data-ttu-id="bd51c-143">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="bd51c-143">East Asia</span></span>
- <span data-ttu-id="bd51c-144">Ausztrália – Kelet</span><span class="sxs-lookup"><span data-stu-id="bd51c-144">Australia East</span></span>
- <span data-ttu-id="bd51c-145">Ausztrália délkeleti</span><span class="sxs-lookup"><span data-stu-id="bd51c-145">Australia Southeast</span></span>

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

### <span data-ttu-id="bd51c-146">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bd51c-146">-Name</span></span>
<span data-ttu-id="bd51c-147">Az API-kezelés bevezetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd51c-147">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="bd51c-148">-Szervezet</span><span class="sxs-lookup"><span data-stu-id="bd51c-148">-Organization</span></span>
<span data-ttu-id="bd51c-149">A szervezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd51c-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="bd51c-150">Az API-kezelés ezt a címet használja a fejlesztői portálon az értesítő e-mailekben.</span><span class="sxs-lookup"><span data-stu-id="bd51c-150">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="bd51c-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd51c-151">-ResourceGroupName</span></span>
<span data-ttu-id="bd51c-152">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt a parancsmag létrehoz egy API-kezelési telepítőt.</span><span class="sxs-lookup"><span data-stu-id="bd51c-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="bd51c-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="bd51c-153">-Sku</span></span>
<span data-ttu-id="bd51c-154">Az API-kezelési szolgáltatás rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd51c-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="bd51c-155">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="bd51c-155">Valid values are:</span></span> 

- <span data-ttu-id="bd51c-156">Fejlesztő</span><span class="sxs-lookup"><span data-stu-id="bd51c-156">Developer</span></span> 
- <span data-ttu-id="bd51c-157">Standard</span><span class="sxs-lookup"><span data-stu-id="bd51c-157">Standard</span></span> 
- <span data-ttu-id="bd51c-158">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="bd51c-158">Premium</span></span> 

<span data-ttu-id="bd51c-159">Az alapértelmezett a fejlesztő.</span><span class="sxs-lookup"><span data-stu-id="bd51c-159">The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd51c-160">-Címkék</span><span class="sxs-lookup"><span data-stu-id="bd51c-160">-Tags</span></span>
<span data-ttu-id="bd51c-161">A címkék szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd51c-161">Specifies a dictionary of tags.</span></span>

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

### <span data-ttu-id="bd51c-162">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bd51c-162">-VirtualNetwork</span></span>
<span data-ttu-id="bd51c-163">Az Azure API felügyeleti központi verziójának virtuális hálózati konfigurációja</span><span class="sxs-lookup"><span data-stu-id="bd51c-163">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="bd51c-164">-VpnType</span><span class="sxs-lookup"><span data-stu-id="bd51c-164">-VpnType</span></span>
<span data-ttu-id="bd51c-165">Az ApiManagement-telepítő virtuális hálózati típusa.</span><span class="sxs-lookup"><span data-stu-id="bd51c-165">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="bd51c-166">Érvényes értékek</span><span class="sxs-lookup"><span data-stu-id="bd51c-166">Valid Values are</span></span> 
- <span data-ttu-id="bd51c-167">"None" (alapértelmezett érték)</span><span class="sxs-lookup"><span data-stu-id="bd51c-167">"None" (Default Value.</span></span> <span data-ttu-id="bd51c-168">A ApiManagement nem része a virtuális hálózatnak ")</span><span class="sxs-lookup"><span data-stu-id="bd51c-168">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="bd51c-169">"Külső" (ApiManagement-telepítés olyan virtuális hálózatban van beállítva, amelynek van internetes végpontja)</span><span class="sxs-lookup"><span data-stu-id="bd51c-169">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="bd51c-170">"Belső" (a ApiManagement-telepítés olyan virtuális hálózatban van beállítva, amelynek intranetes végpontja van)</span><span class="sxs-lookup"><span data-stu-id="bd51c-170">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="bd51c-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd51c-171">-DefaultProfile</span></span>
<span data-ttu-id="bd51c-172">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd51c-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd51c-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd51c-173">CommonParameters</span></span>
<span data-ttu-id="bd51c-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd51c-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd51c-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd51c-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd51c-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd51c-176">INPUTS</span></span>

## <span data-ttu-id="bd51c-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd51c-177">OUTPUTS</span></span>

### <span data-ttu-id="bd51c-178">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="bd51c-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="bd51c-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd51c-179">NOTES</span></span>

## <span data-ttu-id="bd51c-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd51c-180">RELATED LINKS</span></span>

[<span data-ttu-id="bd51c-181">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="bd51c-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="bd51c-182">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="bd51c-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="bd51c-183">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="bd51c-183">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="bd51c-184">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="bd51c-184">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


