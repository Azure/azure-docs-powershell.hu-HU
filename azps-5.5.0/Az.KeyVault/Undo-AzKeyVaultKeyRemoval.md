---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: d6637b8c180dd2ef25bdba5326f0a42a364bc8ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152683"
---
# <span data-ttu-id="d79ff-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="d79ff-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="d79ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d79ff-102">SYNOPSIS</span></span>
<span data-ttu-id="d79ff-103">Egy kulcstár törölt kulcsát aktív állapotba visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="d79ff-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="d79ff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d79ff-104">SYNTAX</span></span>

### <span data-ttu-id="d79ff-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d79ff-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d79ff-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="d79ff-106">HsmInteractive</span></span>
```
Undo-AzKeyVaultKeyRemoval -HsmName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d79ff-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d79ff-107">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d79ff-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d79ff-108">DESCRIPTION</span></span>
<span data-ttu-id="d79ff-109">Az **Undo-AzKeyVaultKeyRemoval** parancsmag helyreállít egy korábban törölt kulcsot.</span><span class="sxs-lookup"><span data-stu-id="d79ff-109">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="d79ff-110">A helyreállított kulcs aktív lesz, és az összes szokásos kulcsművelethez használható.</span><span class="sxs-lookup"><span data-stu-id="d79ff-110">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="d79ff-111">A művelet végrehajtásához a hívónak "helyreállítás" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="d79ff-111">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="d79ff-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d79ff-112">EXAMPLES</span></span>

### <span data-ttu-id="d79ff-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="d79ff-113">Example 1</span></span>
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

<span data-ttu-id="d79ff-114">Ez a parancs aktív és használható állapotba visszaállítja a korábban törölt "MyKey" kulcsot.</span><span class="sxs-lookup"><span data-stu-id="d79ff-114">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="d79ff-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d79ff-115">PARAMETERS</span></span>

### <span data-ttu-id="d79ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79ff-116">-DefaultProfile</span></span>
<span data-ttu-id="d79ff-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d79ff-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d79ff-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="d79ff-118">-HsmName</span></span>
<span data-ttu-id="d79ff-119">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="d79ff-119">HSM name.</span></span> <span data-ttu-id="d79ff-120">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="d79ff-120">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79ff-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d79ff-121">-InputObject</span></span>
<span data-ttu-id="d79ff-122">Kulcsobjektum törlése</span><span class="sxs-lookup"><span data-stu-id="d79ff-122">Deleted key object</span></span>

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

### <span data-ttu-id="d79ff-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d79ff-123">-Name</span></span>
<span data-ttu-id="d79ff-124">Kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="d79ff-124">Key name.</span></span>
<span data-ttu-id="d79ff-125">A parancsmag a tárolónévből (jelenleg kijelölt környezetből és kulcsnévből) egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="d79ff-125">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79ff-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d79ff-126">-VaultName</span></span>
<span data-ttu-id="d79ff-127">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="d79ff-127">Vault name.</span></span>
<span data-ttu-id="d79ff-128">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="d79ff-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d79ff-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d79ff-129">-Confirm</span></span>
<span data-ttu-id="d79ff-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d79ff-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d79ff-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d79ff-131">-WhatIf</span></span>
<span data-ttu-id="d79ff-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d79ff-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d79ff-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d79ff-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d79ff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79ff-134">CommonParameters</span></span>
<span data-ttu-id="d79ff-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d79ff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79ff-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d79ff-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79ff-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d79ff-137">INPUTS</span></span>

### <span data-ttu-id="d79ff-138">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d79ff-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="d79ff-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d79ff-139">OUTPUTS</span></span>

### <span data-ttu-id="d79ff-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d79ff-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="d79ff-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d79ff-141">NOTES</span></span>

## <span data-ttu-id="d79ff-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d79ff-142">RELATED LINKS</span></span>

[<span data-ttu-id="d79ff-143">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d79ff-143">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="d79ff-144">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d79ff-144">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="d79ff-145">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d79ff-145">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

