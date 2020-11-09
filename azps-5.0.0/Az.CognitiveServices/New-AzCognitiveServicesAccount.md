---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 0c7e22174b0306a3b9b5a37bd99edeb06f124334
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299666"
---
# <span data-ttu-id="96c75-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="96c75-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="96c75-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96c75-102">SYNOPSIS</span></span>
<span data-ttu-id="96c75-103">Kognitív szolgáltatások fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="96c75-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="96c75-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96c75-104">SYNTAX</span></span>

### <span data-ttu-id="96c75-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="96c75-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c75-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="96c75-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96c75-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="96c75-107">DESCRIPTION</span></span>
<span data-ttu-id="96c75-108">A **New-AzCognitiveServicesAccount** parancsmag a megadott típusú és SKU-hoz létrehoz egy kognitív szolgáltatásokat tartalmazó fiókot.</span><span class="sxs-lookup"><span data-stu-id="96c75-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="96c75-109">Példák</span><span class="sxs-lookup"><span data-stu-id="96c75-109">EXAMPLES</span></span>

### <span data-ttu-id="96c75-110">1:</span><span class="sxs-lookup"><span data-stu-id="96c75-110">1:</span></span>
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

## <span data-ttu-id="96c75-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96c75-111">PARAMETERS</span></span>

### <span data-ttu-id="96c75-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="96c75-112">-ApiProperty</span></span>
<span data-ttu-id="96c75-113">A ApiProperties (kognitív szolgáltatások) fiók.</span><span class="sxs-lookup"><span data-stu-id="96c75-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="96c75-114">Bizonyos típusú fiókokhoz szükséges.</span><span class="sxs-lookup"><span data-stu-id="96c75-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="96c75-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="96c75-115">-AssignIdentity</span></span>
<span data-ttu-id="96c75-116">Új kognitív szolgáltatások fiók identitásának létrehozása és hozzárendelése az alábbi tárterület-kezeléshez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="96c75-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="96c75-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="96c75-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="96c75-118">Megadhatja, hogy a kognitív szolgáltatásokhoz tartozó titkosítási forrást a Microsoft. CognitiveServices-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="96c75-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="96c75-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="96c75-119">-CustomSubdomainName</span></span>
<span data-ttu-id="96c75-120">A kognitív szolgáltatások fiók altartományának neve.</span><span class="sxs-lookup"><span data-stu-id="96c75-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="96c75-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c75-121">-DefaultProfile</span></span>
<span data-ttu-id="96c75-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="96c75-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96c75-123">-Force</span><span class="sxs-lookup"><span data-stu-id="96c75-123">-Force</span></span>
<span data-ttu-id="96c75-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="96c75-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96c75-125">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="96c75-125">-KeyName</span></span>
<span data-ttu-id="96c75-126">A kognitív szolgáltatások fiókjának titkosítási forráskódja</span><span class="sxs-lookup"><span data-stu-id="96c75-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="96c75-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="96c75-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="96c75-128">Megadhatja, hogy a kognitív szolgáltatásokhoz tartozó titkosítási forráskódot szeretné-e beállítani a Microsoft. vagy sem a Boltozatra.</span><span class="sxs-lookup"><span data-stu-id="96c75-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="96c75-129">Ha a kulcsnév, a verzió-és a KeyVaultUri, a kognitív szolgáltatások-fiók titkosítási forráskódját is megadhatja a Microsoftnak.</span><span class="sxs-lookup"><span data-stu-id="96c75-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="96c75-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="96c75-130">-KeyVaultUri</span></span>
<span data-ttu-id="96c75-131">A kognitív szolgáltatások fiók titkosítási KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="96c75-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="96c75-132">-Verzió</span><span class="sxs-lookup"><span data-stu-id="96c75-132">-KeyVersion</span></span>
<span data-ttu-id="96c75-133">A kognitív szolgáltatások fiókjának titkosítási forráskódja</span><span class="sxs-lookup"><span data-stu-id="96c75-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="96c75-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="96c75-134">-Location</span></span>
<span data-ttu-id="96c75-135">Azt a helyet adja meg, ahol létre szeretné hozni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="96c75-135">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="96c75-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96c75-136">-Name</span></span>
<span data-ttu-id="96c75-137">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96c75-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="96c75-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="96c75-138">-NetworkRuleSet</span></span>
<span data-ttu-id="96c75-139">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazát, valamint a hálózati tulajdonságok értékének beállítását, például az olyan kérelmek kezelését ismerteti, amelyek nem felelnek meg a megadott szabályoknak</span><span class="sxs-lookup"><span data-stu-id="96c75-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="96c75-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="96c75-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="96c75-141">A kognitív szolgáltatások fiók hálózati hozzáférés típusa.</span><span class="sxs-lookup"><span data-stu-id="96c75-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="96c75-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c75-142">-ResourceGroupName</span></span>
<span data-ttu-id="96c75-143">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez hozzá szeretné rendelni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="96c75-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="96c75-144">Az erőforráscsoportnek már léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="96c75-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="96c75-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="96c75-145">-SkuName</span></span>
<span data-ttu-id="96c75-146">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="96c75-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="96c75-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="96c75-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96c75-148">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="96c75-148">F0 (free tier)</span></span>
- <span data-ttu-id="96c75-149">S0</span><span class="sxs-lookup"><span data-stu-id="96c75-149">S0</span></span>
- <span data-ttu-id="96c75-150">S1</span><span class="sxs-lookup"><span data-stu-id="96c75-150">S1</span></span>
- <span data-ttu-id="96c75-151">S2</span><span class="sxs-lookup"><span data-stu-id="96c75-151">S2</span></span>
- <span data-ttu-id="96c75-152">S3</span><span class="sxs-lookup"><span data-stu-id="96c75-152">S3</span></span>
- <span data-ttu-id="96c75-153">S4 további tudnivalókért olvassa el a [kognitív szolgáltatás API](https://www.microsoft.com/cognitive-services/en-us/apis)-k című témakört.</span><span class="sxs-lookup"><span data-stu-id="96c75-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="96c75-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="96c75-154">-StorageAccountId</span></span>
<span data-ttu-id="96c75-155">A felhasználók tulajdonában lévő tárolási fiókjainak listája.</span><span class="sxs-lookup"><span data-stu-id="96c75-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="96c75-156">-Címke</span><span class="sxs-lookup"><span data-stu-id="96c75-156">-Tag</span></span>
<span data-ttu-id="96c75-157">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="96c75-157">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="96c75-158">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="96c75-158">-Type</span></span>
<span data-ttu-id="96c75-159">A létrehozandó fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="96c75-159">Specifies the type of account to create.</span></span> <span data-ttu-id="96c75-160">Használja `Get-AzCognitiveServicesAccountType` a parancsmagot a jelenlegi elfogadható értékek beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="96c75-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="96c75-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96c75-161">-Confirm</span></span>
<span data-ttu-id="96c75-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96c75-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96c75-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c75-163">-WhatIf</span></span>
<span data-ttu-id="96c75-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96c75-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96c75-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96c75-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96c75-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c75-166">CommonParameters</span></span>
<span data-ttu-id="96c75-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96c75-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c75-168">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="96c75-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c75-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96c75-169">INPUTS</span></span>

### <span data-ttu-id="96c75-170">System. String</span><span class="sxs-lookup"><span data-stu-id="96c75-170">System.String</span></span>

## <span data-ttu-id="96c75-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96c75-171">OUTPUTS</span></span>

### <span data-ttu-id="96c75-172">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="96c75-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="96c75-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96c75-173">NOTES</span></span>

## <span data-ttu-id="96c75-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96c75-174">RELATED LINKS</span></span>

[<span data-ttu-id="96c75-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="96c75-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="96c75-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="96c75-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="96c75-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="96c75-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
