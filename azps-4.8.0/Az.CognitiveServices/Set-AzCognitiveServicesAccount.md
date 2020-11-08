---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 5cfbfa0452fba4d01d2af5aa8e6acc3a141a4426
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181202"
---
# <span data-ttu-id="cbf02-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cbf02-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="cbf02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbf02-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf02-103">Módosítja a fiókot.</span><span class="sxs-lookup"><span data-stu-id="cbf02-103">Modifies an account.</span></span>

## <span data-ttu-id="cbf02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbf02-104">SYNTAX</span></span>

### <span data-ttu-id="cbf02-105">CognitiveServicesEncryption (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cbf02-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbf02-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="cbf02-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbf02-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbf02-107">DESCRIPTION</span></span>
<span data-ttu-id="cbf02-108">A **set-AzCognitiveServicesAccount** parancsmag a megadott kognitív Services-fiók SKU-ának vagy címkéjének módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="cbf02-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="cbf02-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cbf02-109">EXAMPLES</span></span>

### <span data-ttu-id="cbf02-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cbf02-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="cbf02-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbf02-111">PARAMETERS</span></span>

### <span data-ttu-id="cbf02-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="cbf02-112">-ApiProperty</span></span>
<span data-ttu-id="cbf02-113">A ApiProperties (kognitív szolgáltatások) fiók.</span><span class="sxs-lookup"><span data-stu-id="cbf02-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="cbf02-114">Bizonyos típusú fiókokhoz szükséges.</span><span class="sxs-lookup"><span data-stu-id="cbf02-114">Required by specific account types.</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="cbf02-115">-AssignIdentity</span></span>
<span data-ttu-id="cbf02-116">Új kognitív szolgáltatások fiók identitásának létrehozása és hozzárendelése az alábbi tárterület-kezeléshez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="cbf02-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="cbf02-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="cbf02-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="cbf02-118">Megadhatja, hogy a kognitív szolgáltatásokhoz tartozó titkosítási forrást a Microsoft. CognitiveServices-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="cbf02-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CognitiveServicesEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="cbf02-119">-CustomSubdomainName</span></span>
<span data-ttu-id="cbf02-120">A kognitív szolgáltatások fiók altartományának neve.</span><span class="sxs-lookup"><span data-stu-id="cbf02-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="cbf02-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf02-121">-DefaultProfile</span></span>
<span data-ttu-id="cbf02-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cbf02-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbf02-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cbf02-123">-Force</span></span>
<span data-ttu-id="cbf02-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="cbf02-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cbf02-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="cbf02-125">-IdentityType</span></span>
<span data-ttu-id="cbf02-126">A felügyelt szolgáltatás identitásának típusa.</span><span class="sxs-lookup"><span data-stu-id="cbf02-126">Type of managed service identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.CognitiveServices.Models.IdentityType]
Parameter Sets: (All)
Aliases:
Accepted values: None, SystemAssigned, UserAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-127">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="cbf02-127">-KeyName</span></span>
<span data-ttu-id="cbf02-128">A kognitív szolgáltatások fiókjának titkosítási forráskódja</span><span class="sxs-lookup"><span data-stu-id="cbf02-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="cbf02-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="cbf02-130">Megadhatja, hogy a kognitív szolgáltatásokhoz tartozó titkosítási forráskódot szeretné-e beállítani a Microsoft. vagy sem a Boltozatra.</span><span class="sxs-lookup"><span data-stu-id="cbf02-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="cbf02-131">Ha a kulcsnév, a verzió-és a KeyVaultUri, a kognitív szolgáltatások-fiók titkosítási forráskódját is megadhatja a Microsoftnak.</span><span class="sxs-lookup"><span data-stu-id="cbf02-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyVaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="cbf02-132">-KeyVaultUri</span></span>
<span data-ttu-id="cbf02-133">A kognitív szolgáltatások fiók titkosítási KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="cbf02-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-134">-Verzió</span><span class="sxs-lookup"><span data-stu-id="cbf02-134">-KeyVersion</span></span>
<span data-ttu-id="cbf02-135">A kognitív szolgáltatások fiókjának titkosítási forráskódja</span><span class="sxs-lookup"><span data-stu-id="cbf02-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cbf02-136">-Name</span></span>
<span data-ttu-id="cbf02-137">A módosítani kívánt fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbf02-137">Specifies the name of the account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cbf02-138">-NetworkRuleSet</span></span>
<span data-ttu-id="cbf02-139">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazát, valamint a hálózati tulajdonságok értékének beállítását, például az olyan kérelmek kezelését ismerteti, amelyek nem felelnek meg a megadott szabályoknak</span><span class="sxs-lookup"><span data-stu-id="cbf02-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="cbf02-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="cbf02-141">A kognitív szolgáltatások fiók hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="cbf02-141">The network access type for Cognitive Services Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf02-142">-ResourceGroupName</span></span>
<span data-ttu-id="cbf02-143">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="cbf02-143">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cbf02-144">-SkuName</span></span>
<span data-ttu-id="cbf02-145">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbf02-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="cbf02-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cbf02-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cbf02-147">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="cbf02-147">F0 (free tier)</span></span>
- <span data-ttu-id="cbf02-148">S0</span><span class="sxs-lookup"><span data-stu-id="cbf02-148">S0</span></span>
- <span data-ttu-id="cbf02-149">S1</span><span class="sxs-lookup"><span data-stu-id="cbf02-149">S1</span></span>
- <span data-ttu-id="cbf02-150">S2</span><span class="sxs-lookup"><span data-stu-id="cbf02-150">S2</span></span>
- <span data-ttu-id="cbf02-151">S3</span><span class="sxs-lookup"><span data-stu-id="cbf02-151">S3</span></span>
- <span data-ttu-id="cbf02-152">S4</span><span class="sxs-lookup"><span data-stu-id="cbf02-152">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cbf02-153">-StorageAccountId</span></span>
<span data-ttu-id="cbf02-154">A felhasználók tulajdonában lévő tárolási fiókjainak listája.</span><span class="sxs-lookup"><span data-stu-id="cbf02-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="cbf02-155">-Címke</span><span class="sxs-lookup"><span data-stu-id="cbf02-155">-Tag</span></span>
<span data-ttu-id="cbf02-156">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="cbf02-156">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-157">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cbf02-157">-Confirm</span></span>
<span data-ttu-id="cbf02-158">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cbf02-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbf02-159">-WhatIf</span></span>
<span data-ttu-id="cbf02-160">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cbf02-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbf02-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cbf02-161">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf02-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf02-162">CommonParameters</span></span>
<span data-ttu-id="cbf02-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbf02-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf02-164">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cbf02-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf02-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbf02-165">INPUTS</span></span>

### <span data-ttu-id="cbf02-166">System. String</span><span class="sxs-lookup"><span data-stu-id="cbf02-166">System.String</span></span>

### <span data-ttu-id="cbf02-167">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="cbf02-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="cbf02-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbf02-168">OUTPUTS</span></span>

### <span data-ttu-id="cbf02-169">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cbf02-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="cbf02-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbf02-170">NOTES</span></span>

## <span data-ttu-id="cbf02-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbf02-171">RELATED LINKS</span></span>

[<span data-ttu-id="cbf02-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cbf02-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="cbf02-173">Új – AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cbf02-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="cbf02-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cbf02-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
