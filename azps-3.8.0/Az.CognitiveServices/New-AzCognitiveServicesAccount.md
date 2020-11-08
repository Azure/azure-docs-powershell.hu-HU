---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 713c5cb34133a233bace576ea80035b8e004eb7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002767"
---
# <span data-ttu-id="278db-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="278db-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="278db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="278db-102">SYNOPSIS</span></span>
<span data-ttu-id="278db-103">Kognitív szolgáltatások fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="278db-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="278db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="278db-104">SYNTAX</span></span>

### <span data-ttu-id="278db-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="278db-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="278db-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="278db-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="278db-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="278db-107">DESCRIPTION</span></span>
<span data-ttu-id="278db-108">A **New-AzCognitiveServicesAccount** parancsmag a megadott típusú és SKU-hoz létrehoz egy kognitív szolgáltatásokat tartalmazó fiókot.</span><span class="sxs-lookup"><span data-stu-id="278db-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="278db-109">Példák</span><span class="sxs-lookup"><span data-stu-id="278db-109">EXAMPLES</span></span>

### <span data-ttu-id="278db-110">1:</span><span class="sxs-lookup"><span data-stu-id="278db-110">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="278db-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="278db-111">PARAMETERS</span></span>

### <span data-ttu-id="278db-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="278db-112">-AssignIdentity</span></span>
<span data-ttu-id="278db-113">Új kognitív szolgáltatások fiók identitásának létrehozása és hozzárendelése az alábbi tárterület-kezeléshez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="278db-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="278db-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="278db-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="278db-115">Megadhatja, hogy a kognitív szolgáltatásokhoz tartozó titkosítási forrást a Microsoft. CognitiveServices-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="278db-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="278db-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="278db-116">-CustomSubdomainName</span></span>
<span data-ttu-id="278db-117">A kognitív szolgáltatások fiók altartományának neve.</span><span class="sxs-lookup"><span data-stu-id="278db-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="278db-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278db-118">-DefaultProfile</span></span>
<span data-ttu-id="278db-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="278db-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="278db-120">-Force</span><span class="sxs-lookup"><span data-stu-id="278db-120">-Force</span></span>
<span data-ttu-id="278db-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="278db-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="278db-122">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="278db-122">-KeyName</span></span>
<span data-ttu-id="278db-123">A kognitív szolgáltatások fiókjának titkosítási forráskódja</span><span class="sxs-lookup"><span data-stu-id="278db-123">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="278db-124">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="278db-124">-KeyVaultEncryption</span></span>
<span data-ttu-id="278db-125">Megadhatja, hogy a kognitív szolgáltatásokhoz tartozó titkosítási forráskódot szeretné-e beállítani a Microsoft. vagy sem a Boltozatra.</span><span class="sxs-lookup"><span data-stu-id="278db-125">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="278db-126">Ha a kulcsnév, a verzió-és a KeyVaultUri, a kognitív szolgáltatások-fiók titkosítási forráskódját is megadhatja a Microsoftnak.</span><span class="sxs-lookup"><span data-stu-id="278db-126">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="278db-127">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="278db-127">-KeyVaultUri</span></span>
<span data-ttu-id="278db-128">A kognitív szolgáltatások fiók titkosítási KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="278db-128">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="278db-129">-Verzió</span><span class="sxs-lookup"><span data-stu-id="278db-129">-KeyVersion</span></span>
<span data-ttu-id="278db-130">A kognitív szolgáltatások fiókjának titkosítási forráskódja</span><span class="sxs-lookup"><span data-stu-id="278db-130">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="278db-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="278db-131">-Location</span></span>
<span data-ttu-id="278db-132">Azt a helyet adja meg, ahol létre szeretné hozni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="278db-132">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="278db-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="278db-133">-Name</span></span>
<span data-ttu-id="278db-134">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="278db-134">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="278db-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="278db-135">-NetworkRuleSet</span></span>
<span data-ttu-id="278db-136">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazát, valamint a hálózati tulajdonságok értékének beállítását, például az olyan kérelmek kezelését ismerteti, amelyek nem felelnek meg a megadott szabályoknak</span><span class="sxs-lookup"><span data-stu-id="278db-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="278db-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="278db-137">-ResourceGroupName</span></span>
<span data-ttu-id="278db-138">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez hozzá szeretné rendelni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="278db-138">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="278db-139">Az erőforráscsoportnek már léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="278db-139">The resource group must already exist.</span></span>

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

### <span data-ttu-id="278db-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="278db-140">-SkuName</span></span>
<span data-ttu-id="278db-141">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="278db-141">Specifies the SKU for the account.</span></span>
<span data-ttu-id="278db-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="278db-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="278db-143">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="278db-143">F0 (free tier)</span></span>
- <span data-ttu-id="278db-144">S0</span><span class="sxs-lookup"><span data-stu-id="278db-144">S0</span></span>
- <span data-ttu-id="278db-145">S1</span><span class="sxs-lookup"><span data-stu-id="278db-145">S1</span></span>
- <span data-ttu-id="278db-146">S2</span><span class="sxs-lookup"><span data-stu-id="278db-146">S2</span></span>
- <span data-ttu-id="278db-147">S3</span><span class="sxs-lookup"><span data-stu-id="278db-147">S3</span></span>
- <span data-ttu-id="278db-148">S4 további tudnivalókért olvassa el a [kognitív szolgáltatás API](https://www.microsoft.com/cognitive-services/en-us/apis)-k című témakört.</span><span class="sxs-lookup"><span data-stu-id="278db-148">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="278db-149">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="278db-149">-StorageAccountId</span></span>
<span data-ttu-id="278db-150">A felhasználók tulajdonában lévő tárolási fiókjainak listája.</span><span class="sxs-lookup"><span data-stu-id="278db-150">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="278db-151">-Címke</span><span class="sxs-lookup"><span data-stu-id="278db-151">-Tag</span></span>
<span data-ttu-id="278db-152">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="278db-152">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278db-153">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="278db-153">-Type</span></span>
<span data-ttu-id="278db-154">A létrehozandó fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="278db-154">Specifies the type of account to create.</span></span> <span data-ttu-id="278db-155">Használja `Get-AzCognitiveServicesAccountType` a parancsmagot a jelenlegi elfogadható értékek beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="278db-155">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="278db-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="278db-156">-Confirm</span></span>
<span data-ttu-id="278db-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="278db-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="278db-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="278db-158">-WhatIf</span></span>
<span data-ttu-id="278db-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="278db-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="278db-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="278db-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="278db-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278db-161">CommonParameters</span></span>
<span data-ttu-id="278db-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="278db-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278db-163">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="278db-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278db-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="278db-164">INPUTS</span></span>

### <span data-ttu-id="278db-165">System. String</span><span class="sxs-lookup"><span data-stu-id="278db-165">System.String</span></span>

## <span data-ttu-id="278db-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="278db-166">OUTPUTS</span></span>

### <span data-ttu-id="278db-167">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="278db-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="278db-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="278db-168">NOTES</span></span>

## <span data-ttu-id="278db-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="278db-169">RELATED LINKS</span></span>

[<span data-ttu-id="278db-170">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="278db-170">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="278db-171">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="278db-171">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="278db-172">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="278db-172">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
