---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 5cfbfa0452fba4d01d2af5aa8e6acc3a141a4426
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358314"
---
# <span data-ttu-id="62b30-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="62b30-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="62b30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62b30-102">SYNOPSIS</span></span>
<span data-ttu-id="62b30-103">Módosít egy fiókot.</span><span class="sxs-lookup"><span data-stu-id="62b30-103">Modifies an account.</span></span>

## <span data-ttu-id="62b30-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="62b30-104">SYNTAX</span></span>

### <span data-ttu-id="62b30-105">CognitiveServicesEncryption (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="62b30-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62b30-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="62b30-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62b30-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="62b30-107">DESCRIPTION</span></span>
<span data-ttu-id="62b30-108">A **Set-AzCognitiveServicesAccount** parancsmag módosítja a megadott Kognitív Szolgáltatások-fiók termékváltozatát vagy címkéit.</span><span class="sxs-lookup"><span data-stu-id="62b30-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="62b30-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="62b30-109">EXAMPLES</span></span>

### <span data-ttu-id="62b30-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="62b30-110">Example 1</span></span>
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

## <span data-ttu-id="62b30-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62b30-111">PARAMETERS</span></span>

### <span data-ttu-id="62b30-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="62b30-112">-ApiProperty</span></span>
<span data-ttu-id="62b30-113">A Kognitív Szolgáltatások fiók ApiProperties.</span><span class="sxs-lookup"><span data-stu-id="62b30-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="62b30-114">Bizonyos fióktípusok kötelezők.</span><span class="sxs-lookup"><span data-stu-id="62b30-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="62b30-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="62b30-115">-AssignIdentity</span></span>
<span data-ttu-id="62b30-116">Létrehozhat és hozzárendelhet egy új Kognitív Szolgáltatások-fiók identitást ehhez a tárfiókhoz, hogy olyan kulcskezelési szolgáltatásokkal használva használja őket, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="62b30-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="62b30-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="62b30-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="62b30-118">Állítsa-e be a Kognitív szolgáltatások fióktitkosítási kulcsforrását a Microsoft.CognitiveServices szolgáltatóra.</span><span class="sxs-lookup"><span data-stu-id="62b30-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="62b30-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="62b30-119">-CustomSubdomainName</span></span>
<span data-ttu-id="62b30-120">Kognitív szolgáltatások fiók altartományának neve.</span><span class="sxs-lookup"><span data-stu-id="62b30-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="62b30-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b30-121">-DefaultProfile</span></span>
<span data-ttu-id="62b30-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="62b30-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62b30-123">-Force</span><span class="sxs-lookup"><span data-stu-id="62b30-123">-Force</span></span>
<span data-ttu-id="62b30-124">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="62b30-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62b30-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="62b30-125">-IdentityType</span></span>
<span data-ttu-id="62b30-126">A felügyelt szolgáltatás identitásának típusa.</span><span class="sxs-lookup"><span data-stu-id="62b30-126">Type of managed service identity.</span></span>

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

### <span data-ttu-id="62b30-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="62b30-127">-KeyName</span></span>
<span data-ttu-id="62b30-128">Cognitive Services Account encryption keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="62b30-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="62b30-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="62b30-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="62b30-130">Állítsa-e be a Kognitív szolgáltatások fiók titkosítási kulcsForrását a Microsoft.KeyVaultra vagy sem.</span><span class="sxs-lookup"><span data-stu-id="62b30-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="62b30-131">Ha a KeyName, a KeyVersion és a KeyVaultUri értéket adja meg, akkor a Kognitív szolgáltatások fióktitkosítási kulcsforrása is a Microsoft.KeyVault időjárási beállítása lesz, ez a paraméter be van-e állítva vagy sem.</span><span class="sxs-lookup"><span data-stu-id="62b30-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="62b30-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="62b30-132">-KeyVaultUri</span></span>
<span data-ttu-id="62b30-133">Kognitív szolgáltatások fióktitkosítási kulcsSource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="62b30-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="62b30-134">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="62b30-134">-KeyVersion</span></span>
<span data-ttu-id="62b30-135">Kognitív szolgáltatások fióktitkosítási kulcsSource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="62b30-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="62b30-136">-Name</span><span class="sxs-lookup"><span data-stu-id="62b30-136">-Name</span></span>
<span data-ttu-id="62b30-137">A módosítani szükséges fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62b30-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="62b30-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="62b30-138">-NetworkRuleSet</span></span>
<span data-ttu-id="62b30-139">A NetworkRuleSet tűzfalakra és virtuális hálózatokra vonatkozó konfigurációs szabályok halmazának meghatározására, valamint a hálózati tulajdonságok értékeinek beállításához használható, például a megadott szabályoktól különböző kérések kezelésére.</span><span class="sxs-lookup"><span data-stu-id="62b30-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="62b30-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="62b30-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="62b30-141">A Cognitive Services-fiók hálózati hozzáférési típusa.</span><span class="sxs-lookup"><span data-stu-id="62b30-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="62b30-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62b30-142">-ResourceGroupName</span></span>
<span data-ttu-id="62b30-143">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="62b30-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="62b30-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="62b30-144">-SkuName</span></span>
<span data-ttu-id="62b30-145">A fiók termékváltozatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="62b30-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="62b30-146">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="62b30-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62b30-147">F0 (ingyenes szint)</span><span class="sxs-lookup"><span data-stu-id="62b30-147">F0 (free tier)</span></span>
- <span data-ttu-id="62b30-148">S0</span><span class="sxs-lookup"><span data-stu-id="62b30-148">S0</span></span>
- <span data-ttu-id="62b30-149">S1</span><span class="sxs-lookup"><span data-stu-id="62b30-149">S1</span></span>
- <span data-ttu-id="62b30-150">S2</span><span class="sxs-lookup"><span data-stu-id="62b30-150">S2</span></span>
- <span data-ttu-id="62b30-151">S3</span><span class="sxs-lookup"><span data-stu-id="62b30-151">S3</span></span>
- <span data-ttu-id="62b30-152">S4</span><span class="sxs-lookup"><span data-stu-id="62b30-152">S4</span></span>

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

### <span data-ttu-id="62b30-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="62b30-153">-StorageAccountId</span></span>
<span data-ttu-id="62b30-154">A felhasználói tárfiókok listája.</span><span class="sxs-lookup"><span data-stu-id="62b30-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="62b30-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="62b30-155">-Tag</span></span>
<span data-ttu-id="62b30-156">Egy címkét ad meg név/érték párként.</span><span class="sxs-lookup"><span data-stu-id="62b30-156">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="62b30-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62b30-157">-Confirm</span></span>
<span data-ttu-id="62b30-158">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="62b30-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62b30-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62b30-159">-WhatIf</span></span>
<span data-ttu-id="62b30-160">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="62b30-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62b30-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62b30-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62b30-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b30-162">CommonParameters</span></span>
<span data-ttu-id="62b30-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62b30-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b30-164">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62b30-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b30-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62b30-165">INPUTS</span></span>

### <span data-ttu-id="62b30-166">System.String</span><span class="sxs-lookup"><span data-stu-id="62b30-166">System.String</span></span>

### <span data-ttu-id="62b30-167">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="62b30-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="62b30-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62b30-168">OUTPUTS</span></span>

### <span data-ttu-id="62b30-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="62b30-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="62b30-170">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="62b30-170">NOTES</span></span>

## <span data-ttu-id="62b30-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62b30-171">RELATED LINKS</span></span>

[<span data-ttu-id="62b30-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="62b30-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="62b30-173">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="62b30-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="62b30-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="62b30-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
