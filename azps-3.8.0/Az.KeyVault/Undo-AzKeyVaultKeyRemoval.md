---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: c2b4fec2524ed3ddac62cf687af33ba3f76f13e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846049"
---
# <span data-ttu-id="829ea-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="829ea-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="829ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="829ea-102">SYNOPSIS</span></span>
<span data-ttu-id="829ea-103">A törölt kulcsok aktív állapotba való visszanyerése.</span><span class="sxs-lookup"><span data-stu-id="829ea-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="829ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="829ea-104">SYNTAX</span></span>

### <span data-ttu-id="829ea-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="829ea-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="829ea-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="829ea-106">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="829ea-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="829ea-107">DESCRIPTION</span></span>
<span data-ttu-id="829ea-108">A **Visszavonás-AzKeyVaultKeyRemoval** parancsmag visszaállítja a korábban törölt kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="829ea-108">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="829ea-109">A helyreállított kulcs aktív lesz, és az összes normál művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="829ea-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="829ea-110">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="829ea-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="829ea-111">Példák</span><span class="sxs-lookup"><span data-stu-id="829ea-111">EXAMPLES</span></span>

### <span data-ttu-id="829ea-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="829ea-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="829ea-113">Ez a parancs a korábban törölt "MyKey" kulcsot aktív és használható állapotba fogja állítani.</span><span class="sxs-lookup"><span data-stu-id="829ea-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="829ea-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="829ea-114">PARAMETERS</span></span>

### <span data-ttu-id="829ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="829ea-115">-DefaultProfile</span></span>
<span data-ttu-id="829ea-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="829ea-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="829ea-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="829ea-117">-InputObject</span></span>
<span data-ttu-id="829ea-118">Törölt kulcs objektum</span><span class="sxs-lookup"><span data-stu-id="829ea-118">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="829ea-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="829ea-119">-Name</span></span>
<span data-ttu-id="829ea-120">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="829ea-120">Key name.</span></span>
<span data-ttu-id="829ea-121">Parancsmag: a kulcs FQDN-je a boltozat neve, az aktuálisan kijelölt környezet és a kulcs neve alapján.</span><span class="sxs-lookup"><span data-stu-id="829ea-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="829ea-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="829ea-122">-VaultName</span></span>
<span data-ttu-id="829ea-123">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="829ea-123">Vault name.</span></span>
<span data-ttu-id="829ea-124">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="829ea-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="829ea-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="829ea-125">-Confirm</span></span>
<span data-ttu-id="829ea-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="829ea-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="829ea-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="829ea-127">-WhatIf</span></span>
<span data-ttu-id="829ea-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="829ea-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="829ea-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="829ea-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="829ea-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="829ea-130">CommonParameters</span></span>
<span data-ttu-id="829ea-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="829ea-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="829ea-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="829ea-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="829ea-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="829ea-133">INPUTS</span></span>

### <span data-ttu-id="829ea-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="829ea-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="829ea-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="829ea-135">OUTPUTS</span></span>

### <span data-ttu-id="829ea-136">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="829ea-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="829ea-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="829ea-137">NOTES</span></span>

## <span data-ttu-id="829ea-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="829ea-138">RELATED LINKS</span></span>

[<span data-ttu-id="829ea-139">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="829ea-139">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="829ea-140">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="829ea-140">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="829ea-141">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="829ea-141">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

