---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: ff4682a7c97f721dac9fb53f375c2a96f4bb33b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666137"
---
# <span data-ttu-id="dfa6e-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="dfa6e-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="dfa6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfa6e-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa6e-103">A törölt kulcsok aktív állapotba való visszanyerése.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="dfa6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfa6e-104">SYNTAX</span></span>

### <span data-ttu-id="dfa6e-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dfa6e-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfa6e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="dfa6e-106">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfa6e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfa6e-107">DESCRIPTION</span></span>
<span data-ttu-id="dfa6e-108">A **Visszavonás-AzKeyVaultKeyRemoval** parancsmag visszaállítja a korábban törölt kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-108">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="dfa6e-109">A helyreállított kulcs aktív lesz, és az összes normál művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="dfa6e-110">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="dfa6e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="dfa6e-111">EXAMPLES</span></span>

### <span data-ttu-id="dfa6e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dfa6e-112">Example 1</span></span>
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

<span data-ttu-id="dfa6e-113">Ez a parancs a korábban törölt "MyKey" kulcsot aktív és használható állapotba fogja állítani.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="dfa6e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfa6e-114">PARAMETERS</span></span>

### <span data-ttu-id="dfa6e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa6e-115">-DefaultProfile</span></span>
<span data-ttu-id="dfa6e-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dfa6e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfa6e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfa6e-117">-InputObject</span></span>
<span data-ttu-id="dfa6e-118">Törölt kulcs objektum</span><span class="sxs-lookup"><span data-stu-id="dfa6e-118">Deleted key object</span></span>

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

### <span data-ttu-id="dfa6e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dfa6e-119">-Name</span></span>
<span data-ttu-id="dfa6e-120">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-120">Key name.</span></span>
<span data-ttu-id="dfa6e-121">Parancsmag: a kulcs FQDN-je a boltozat neve, az aktuálisan kijelölt környezet és a kulcs neve alapján.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="dfa6e-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dfa6e-122">-VaultName</span></span>
<span data-ttu-id="dfa6e-123">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-123">Vault name.</span></span>
<span data-ttu-id="dfa6e-124">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="dfa6e-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dfa6e-125">-Confirm</span></span>
<span data-ttu-id="dfa6e-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfa6e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfa6e-127">-WhatIf</span></span>
<span data-ttu-id="dfa6e-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfa6e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfa6e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa6e-130">CommonParameters</span></span>
<span data-ttu-id="dfa6e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfa6e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa6e-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfa6e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa6e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfa6e-133">INPUTS</span></span>

### <span data-ttu-id="dfa6e-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="dfa6e-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="dfa6e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfa6e-135">OUTPUTS</span></span>

### <span data-ttu-id="dfa6e-136">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="dfa6e-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfa6e-137">NOTES</span></span>

## <span data-ttu-id="dfa6e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfa6e-138">RELATED LINKS</span></span>

[<span data-ttu-id="dfa6e-139">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dfa6e-139">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="dfa6e-140">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dfa6e-140">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="dfa6e-141">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dfa6e-141">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

