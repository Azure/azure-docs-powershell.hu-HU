---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: 6de9fecc4b9576f9d69ddc1f963ae537f4422371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503632"
---
# <span data-ttu-id="1d39b-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="1d39b-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="1d39b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d39b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d39b-103">A törölt kulcsok aktív állapotba való visszanyerése.</span><span class="sxs-lookup"><span data-stu-id="1d39b-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d39b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d39b-104">SYNTAX</span></span>

### <span data-ttu-id="1d39b-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d39b-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d39b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1d39b-106">InputObject</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d39b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d39b-107">DESCRIPTION</span></span>
<span data-ttu-id="1d39b-108">A **Visszavonás-AzureKeyVaultKeyRemoval** parancsmag visszaállítja a korábban törölt kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="1d39b-108">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="1d39b-109">A helyreállított kulcs aktív lesz, és az összes normál művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="1d39b-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="1d39b-110">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="1d39b-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="1d39b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1d39b-111">EXAMPLES</span></span>

### <span data-ttu-id="1d39b-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1d39b-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

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

<span data-ttu-id="1d39b-113">Ez a parancs a korábban törölt "MyKey" kulcsot aktív és használható állapotba fogja állítani.</span><span class="sxs-lookup"><span data-stu-id="1d39b-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="1d39b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d39b-114">PARAMETERS</span></span>

### <span data-ttu-id="1d39b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d39b-115">-DefaultProfile</span></span>
<span data-ttu-id="1d39b-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1d39b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d39b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d39b-117">-InputObject</span></span>
<span data-ttu-id="1d39b-118">Törölt kulcs objektum</span><span class="sxs-lookup"><span data-stu-id="1d39b-118">Deleted key object</span></span>

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

### <span data-ttu-id="1d39b-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d39b-119">-Name</span></span>
<span data-ttu-id="1d39b-120">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="1d39b-120">Key name.</span></span>
<span data-ttu-id="1d39b-121">Parancsmag: a kulcs FQDN-je a boltozat neve, az aktuálisan kijelölt környezet és a kulcs neve alapján.</span><span class="sxs-lookup"><span data-stu-id="1d39b-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="1d39b-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1d39b-122">-VaultName</span></span>
<span data-ttu-id="1d39b-123">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="1d39b-123">Vault name.</span></span>
<span data-ttu-id="1d39b-124">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="1d39b-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1d39b-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1d39b-125">-Confirm</span></span>
<span data-ttu-id="1d39b-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d39b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d39b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d39b-127">-WhatIf</span></span>
<span data-ttu-id="1d39b-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1d39b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d39b-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d39b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d39b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d39b-130">CommonParameters</span></span>
<span data-ttu-id="1d39b-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d39b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d39b-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d39b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d39b-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d39b-133">INPUTS</span></span>

### <span data-ttu-id="1d39b-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1d39b-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="1d39b-135">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1d39b-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1d39b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d39b-136">OUTPUTS</span></span>

### <span data-ttu-id="1d39b-137">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="1d39b-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="1d39b-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d39b-138">NOTES</span></span>

## <span data-ttu-id="1d39b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d39b-139">RELATED LINKS</span></span>

[<span data-ttu-id="1d39b-140">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1d39b-140">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="1d39b-141">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1d39b-141">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="1d39b-142">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1d39b-142">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

