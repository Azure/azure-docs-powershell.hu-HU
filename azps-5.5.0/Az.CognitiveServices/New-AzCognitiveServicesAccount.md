---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 0c7e22174b0306a3b9b5a37bd99edeb06f124334
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210158"
---
# <span data-ttu-id="59bd6-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="59bd6-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="59bd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="59bd6-103">Kognitív szolgáltatások fiókját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="59bd6-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="59bd6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59bd6-104">SYNTAX</span></span>

### <span data-ttu-id="59bd6-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="59bd6-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59bd6-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="59bd6-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59bd6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59bd6-107">DESCRIPTION</span></span>
<span data-ttu-id="59bd6-108">A **New-AzCognitiveServicesAccount** parancsmag létrehoz egy kognitív szolgáltatások fiókot a megadott típussal és termékváltozatmal.</span><span class="sxs-lookup"><span data-stu-id="59bd6-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="59bd6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59bd6-109">EXAMPLES</span></span>

### <span data-ttu-id="59bd6-110">1:</span><span class="sxs-lookup"><span data-stu-id="59bd6-110">1:</span></span>
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

## <span data-ttu-id="59bd6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59bd6-111">PARAMETERS</span></span>

### <span data-ttu-id="59bd6-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="59bd6-112">-ApiProperty</span></span>
<span data-ttu-id="59bd6-113">A Kognitív Szolgáltatások fiók ApiProperties.</span><span class="sxs-lookup"><span data-stu-id="59bd6-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="59bd6-114">Bizonyos fióktípusok kötelezők.</span><span class="sxs-lookup"><span data-stu-id="59bd6-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="59bd6-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="59bd6-115">-AssignIdentity</span></span>
<span data-ttu-id="59bd6-116">Létrehozhat és hozzárendelhet egy új Kognitív Szolgáltatások-fiók identitást ehhez a tárfiókhoz, hogy olyan kulcskezelési szolgáltatásokkal használva használja őket, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="59bd6-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="59bd6-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="59bd6-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="59bd6-118">Állítsa-e be a Kognitív szolgáltatások fióktitkosítási kulcsforrását a Microsoft.CognitiveServices szolgáltatóra.</span><span class="sxs-lookup"><span data-stu-id="59bd6-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="59bd6-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="59bd6-119">-CustomSubdomainName</span></span>
<span data-ttu-id="59bd6-120">Kognitív szolgáltatások fiók altartományának neve.</span><span class="sxs-lookup"><span data-stu-id="59bd6-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="59bd6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59bd6-121">-DefaultProfile</span></span>
<span data-ttu-id="59bd6-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="59bd6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59bd6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="59bd6-123">-Force</span></span>
<span data-ttu-id="59bd6-124">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="59bd6-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="59bd6-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="59bd6-125">-KeyName</span></span>
<span data-ttu-id="59bd6-126">Cognitive Services Account encryption keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="59bd6-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="59bd6-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="59bd6-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="59bd6-128">A Kognitív szolgáltatások fiók titkosítási kulcsForrás beállítása a Microsoft.KeyVaultra vagy sem.</span><span class="sxs-lookup"><span data-stu-id="59bd6-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="59bd6-129">Ha a KeyName, a KeyVersion és a KeyVaultUri értéket adja meg, akkor a Kognitív szolgáltatások fióktitkosítási kulcsforrása is a Microsoft.KeyVault időjárási beállítása lesz, ez a paraméter be van-e állítva vagy sem.</span><span class="sxs-lookup"><span data-stu-id="59bd6-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="59bd6-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="59bd6-130">-KeyVaultUri</span></span>
<span data-ttu-id="59bd6-131">Kognitív szolgáltatások fióktitkosítási kulcsSource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="59bd6-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="59bd6-132">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="59bd6-132">-KeyVersion</span></span>
<span data-ttu-id="59bd6-133">Kognitív szolgáltatások fióktitkosítási kulcsSource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="59bd6-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="59bd6-134">-Location</span><span class="sxs-lookup"><span data-stu-id="59bd6-134">-Location</span></span>
<span data-ttu-id="59bd6-135">Azt a helyet adja meg, ahol létre kell hoznia a fiókot.</span><span class="sxs-lookup"><span data-stu-id="59bd6-135">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="59bd6-136">-Name</span><span class="sxs-lookup"><span data-stu-id="59bd6-136">-Name</span></span>
<span data-ttu-id="59bd6-137">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59bd6-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="59bd6-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="59bd6-138">-NetworkRuleSet</span></span>
<span data-ttu-id="59bd6-139">A NetworkRuleSet tűzfalakra és virtuális hálózatokra vonatkozó konfigurációs szabályok halmazának meghatározására, valamint a hálózati tulajdonságok értékeinek beállításához használható, például a megadott szabályoktól különböző kérések kezelésére.</span><span class="sxs-lookup"><span data-stu-id="59bd6-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="59bd6-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="59bd6-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="59bd6-141">A Cognitive Services-fiók hálózati hozzáférési típusa.</span><span class="sxs-lookup"><span data-stu-id="59bd6-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="59bd6-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59bd6-142">-ResourceGroupName</span></span>
<span data-ttu-id="59bd6-143">Annak az erőforráscsoportnak a nevét adja meg, amelyhez hozzá kell rendelni a fiókot.</span><span class="sxs-lookup"><span data-stu-id="59bd6-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="59bd6-144">Az erőforráscsoportnak már léteznie kell.</span><span class="sxs-lookup"><span data-stu-id="59bd6-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="59bd6-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="59bd6-145">-SkuName</span></span>
<span data-ttu-id="59bd6-146">A fiók termékváltozatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59bd6-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="59bd6-147">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="59bd6-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59bd6-148">F0 (ingyenes szint)</span><span class="sxs-lookup"><span data-stu-id="59bd6-148">F0 (free tier)</span></span>
- <span data-ttu-id="59bd6-149">S0</span><span class="sxs-lookup"><span data-stu-id="59bd6-149">S0</span></span>
- <span data-ttu-id="59bd6-150">S1</span><span class="sxs-lookup"><span data-stu-id="59bd6-150">S1</span></span>
- <span data-ttu-id="59bd6-151">S2</span><span class="sxs-lookup"><span data-stu-id="59bd6-151">S2</span></span>
- <span data-ttu-id="59bd6-152">S3</span><span class="sxs-lookup"><span data-stu-id="59bd6-152">S3</span></span>
- <span data-ttu-id="59bd6-153">S4 További információért [lásd: Kognitív szolgáltatás API-k.](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="59bd6-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="59bd6-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="59bd6-154">-StorageAccountId</span></span>
<span data-ttu-id="59bd6-155">A felhasználói tárfiókok listája.</span><span class="sxs-lookup"><span data-stu-id="59bd6-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="59bd6-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="59bd6-156">-Tag</span></span>
<span data-ttu-id="59bd6-157">Egy címkét ad meg név/érték párként.</span><span class="sxs-lookup"><span data-stu-id="59bd6-157">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="59bd6-158">-Type</span><span class="sxs-lookup"><span data-stu-id="59bd6-158">-Type</span></span>
<span data-ttu-id="59bd6-159">A létrehozni szükséges fiók típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="59bd6-159">Specifies the type of account to create.</span></span> <span data-ttu-id="59bd6-160">A `Get-AzCognitiveServicesAccountType` parancsmagot használva aktuális elfogadható értékeket kap.</span><span class="sxs-lookup"><span data-stu-id="59bd6-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="59bd6-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59bd6-161">-Confirm</span></span>
<span data-ttu-id="59bd6-162">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="59bd6-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59bd6-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59bd6-163">-WhatIf</span></span>
<span data-ttu-id="59bd6-164">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="59bd6-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59bd6-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59bd6-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59bd6-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bd6-166">CommonParameters</span></span>
<span data-ttu-id="59bd6-167">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59bd6-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bd6-168">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59bd6-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bd6-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59bd6-169">INPUTS</span></span>

### <span data-ttu-id="59bd6-170">System.String</span><span class="sxs-lookup"><span data-stu-id="59bd6-170">System.String</span></span>

## <span data-ttu-id="59bd6-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59bd6-171">OUTPUTS</span></span>

### <span data-ttu-id="59bd6-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="59bd6-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="59bd6-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59bd6-173">NOTES</span></span>

## <span data-ttu-id="59bd6-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59bd6-174">RELATED LINKS</span></span>

[<span data-ttu-id="59bd6-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="59bd6-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="59bd6-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="59bd6-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="59bd6-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="59bd6-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
