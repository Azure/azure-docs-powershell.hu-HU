---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: fc510ebede11168dd8d8b090cd2069ce3e6de52c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002754"
---
# <span data-ttu-id="52e17-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="52e17-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="52e17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52e17-102">SYNOPSIS</span></span>
<span data-ttu-id="52e17-103">Módosítja a fiókot.</span><span class="sxs-lookup"><span data-stu-id="52e17-103">Modifies an account.</span></span>

## <span data-ttu-id="52e17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52e17-104">SYNTAX</span></span>

### <span data-ttu-id="52e17-105">CognitiveServicesEncryption (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52e17-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52e17-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="52e17-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52e17-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="52e17-107">DESCRIPTION</span></span>
<span data-ttu-id="52e17-108">A **set-AzCognitiveServicesAccount** parancsmag a megadott kognitív Services-fiók SKU-ának vagy címkéjének módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="52e17-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="52e17-109">Példák</span><span class="sxs-lookup"><span data-stu-id="52e17-109">EXAMPLES</span></span>

### <span data-ttu-id="52e17-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="52e17-110">Example 1</span></span>
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

## <span data-ttu-id="52e17-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52e17-111">PARAMETERS</span></span>

### <span data-ttu-id="52e17-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="52e17-112">-AssignIdentity</span></span>
<span data-ttu-id="52e17-113">Új kognitív szolgáltatások fiók identitásának létrehozása és hozzárendelése az alábbi tárterület-kezeléshez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="52e17-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="52e17-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="52e17-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="52e17-115">Megadhatja, hogy a kognitív szolgáltatásokhoz tartozó titkosítási forrást a Microsoft. CognitiveServices-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="52e17-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="52e17-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="52e17-116">-CustomSubdomainName</span></span>
<span data-ttu-id="52e17-117">A kognitív szolgáltatások fiók altartományának neve.</span><span class="sxs-lookup"><span data-stu-id="52e17-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="52e17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52e17-118">-DefaultProfile</span></span>
<span data-ttu-id="52e17-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="52e17-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52e17-120">-Force</span><span class="sxs-lookup"><span data-stu-id="52e17-120">-Force</span></span>
<span data-ttu-id="52e17-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="52e17-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="52e17-122">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="52e17-122">-IdentityType</span></span>
<span data-ttu-id="52e17-123">A felügyelt szolgáltatás identitásának típusa.</span><span class="sxs-lookup"><span data-stu-id="52e17-123">Type of managed service identity.</span></span>

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

### <span data-ttu-id="52e17-124">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="52e17-124">-KeyName</span></span>
<span data-ttu-id="52e17-125">A kognitív szolgáltatások fiókjának titkosítási forráskódja</span><span class="sxs-lookup"><span data-stu-id="52e17-125">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="52e17-126">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="52e17-126">-KeyVaultEncryption</span></span>
<span data-ttu-id="52e17-127">Megadhatja, hogy a kognitív szolgáltatásokhoz tartozó titkosítási forráskódot szeretné-e beállítani a Microsoft. vagy sem a Boltozatra.</span><span class="sxs-lookup"><span data-stu-id="52e17-127">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="52e17-128">Ha a kulcsnév, a verzió-és a KeyVaultUri, a kognitív szolgáltatások-fiók titkosítási forráskódját is megadhatja a Microsoftnak.</span><span class="sxs-lookup"><span data-stu-id="52e17-128">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="52e17-129">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="52e17-129">-KeyVaultUri</span></span>
<span data-ttu-id="52e17-130">A kognitív szolgáltatások fiók titkosítási KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="52e17-130">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="52e17-131">-Verzió</span><span class="sxs-lookup"><span data-stu-id="52e17-131">-KeyVersion</span></span>
<span data-ttu-id="52e17-132">A kognitív szolgáltatások fiókjának titkosítási forráskódja</span><span class="sxs-lookup"><span data-stu-id="52e17-132">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="52e17-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="52e17-133">-Name</span></span>
<span data-ttu-id="52e17-134">A módosítani kívánt fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52e17-134">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="52e17-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="52e17-135">-NetworkRuleSet</span></span>
<span data-ttu-id="52e17-136">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazát, valamint a hálózati tulajdonságok értékének beállítását, például az olyan kérelmek kezelését ismerteti, amelyek nem felelnek meg a megadott szabályoknak</span><span class="sxs-lookup"><span data-stu-id="52e17-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="52e17-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52e17-137">-ResourceGroupName</span></span>
<span data-ttu-id="52e17-138">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="52e17-138">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="52e17-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="52e17-139">-SkuName</span></span>
<span data-ttu-id="52e17-140">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="52e17-140">Specifies the SKU for the account.</span></span>
<span data-ttu-id="52e17-141">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="52e17-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="52e17-142">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="52e17-142">F0 (free tier)</span></span>
- <span data-ttu-id="52e17-143">S0</span><span class="sxs-lookup"><span data-stu-id="52e17-143">S0</span></span>
- <span data-ttu-id="52e17-144">S1</span><span class="sxs-lookup"><span data-stu-id="52e17-144">S1</span></span>
- <span data-ttu-id="52e17-145">S2</span><span class="sxs-lookup"><span data-stu-id="52e17-145">S2</span></span>
- <span data-ttu-id="52e17-146">S3</span><span class="sxs-lookup"><span data-stu-id="52e17-146">S3</span></span>
- <span data-ttu-id="52e17-147">S4</span><span class="sxs-lookup"><span data-stu-id="52e17-147">S4</span></span>

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

### <span data-ttu-id="52e17-148">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="52e17-148">-StorageAccountId</span></span>
<span data-ttu-id="52e17-149">A felhasználók tulajdonában lévő tárolási fiókjainak listája.</span><span class="sxs-lookup"><span data-stu-id="52e17-149">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="52e17-150">-Címke</span><span class="sxs-lookup"><span data-stu-id="52e17-150">-Tag</span></span>
<span data-ttu-id="52e17-151">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="52e17-151">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="52e17-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="52e17-152">-Confirm</span></span>
<span data-ttu-id="52e17-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="52e17-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52e17-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52e17-154">-WhatIf</span></span>
<span data-ttu-id="52e17-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="52e17-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52e17-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52e17-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52e17-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e17-157">CommonParameters</span></span>
<span data-ttu-id="52e17-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52e17-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e17-159">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="52e17-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e17-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52e17-160">INPUTS</span></span>

### <span data-ttu-id="52e17-161">System. String</span><span class="sxs-lookup"><span data-stu-id="52e17-161">System.String</span></span>

### <span data-ttu-id="52e17-162">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="52e17-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="52e17-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52e17-163">OUTPUTS</span></span>

### <span data-ttu-id="52e17-164">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="52e17-164">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="52e17-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52e17-165">NOTES</span></span>

## <span data-ttu-id="52e17-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52e17-166">RELATED LINKS</span></span>

[<span data-ttu-id="52e17-167">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="52e17-167">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="52e17-168">Új – AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="52e17-168">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="52e17-169">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="52e17-169">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
