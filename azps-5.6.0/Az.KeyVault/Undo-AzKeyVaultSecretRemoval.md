---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: dc4c8925d4ddf00cc2e2739d3aa06285f628e423
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931113"
---
# <span data-ttu-id="4c352-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="4c352-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="4c352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c352-102">SYNOPSIS</span></span>
<span data-ttu-id="4c352-103">Egy kulcstár törölt titkos kulcsát aktív állapotba helyreállítja.</span><span class="sxs-lookup"><span data-stu-id="4c352-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="4c352-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4c352-104">SYNTAX</span></span>

### <span data-ttu-id="4c352-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c352-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c352-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4c352-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c352-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4c352-107">DESCRIPTION</span></span>
<span data-ttu-id="4c352-108">Az **Undo-AzKeyVaultSecretRemoval** parancsmag helyreállít egy korábban törölt titkos adatokat.</span><span class="sxs-lookup"><span data-stu-id="4c352-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="4c352-109">A helyreállított titkos titkos művelet aktív lesz, és minden normál titkos művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="4c352-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="4c352-110">A művelet végrehajtásához a hívónak "helyreállítás" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="4c352-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="4c352-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4c352-111">EXAMPLES</span></span>

### <span data-ttu-id="4c352-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="4c352-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

Vault Name   : MyKeyVault
Name         : MySecret
Version      : f622abc7b1394092812f1eb0f85dc91c
Id           : https://mykeyvault.vault.azure.net:443/secrets/mysecret/f622abc7b1394092812f1eb0f85dc91c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/19/2018 5:56:02 PM
Updated      : 4/26/2018 7:48:40 PM
Content Type :
Tags         :
```

<span data-ttu-id="4c352-113">Ez a parancs egy aktív és használható állapotba visszaállítja a korábban törölt "MySecret" titkos fájlt.</span><span class="sxs-lookup"><span data-stu-id="4c352-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="4c352-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c352-114">PARAMETERS</span></span>

### <span data-ttu-id="4c352-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c352-115">-DefaultProfile</span></span>
<span data-ttu-id="4c352-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4c352-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c352-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c352-117">-InputObject</span></span>
<span data-ttu-id="4c352-118">Titkos objektum törlése</span><span class="sxs-lookup"><span data-stu-id="4c352-118">Deleted secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c352-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4c352-119">-Name</span></span>
<span data-ttu-id="4c352-120">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="4c352-120">Secret name.</span></span>
<span data-ttu-id="4c352-121">A parancsmag a tárolónévből ( jelenleg kijelölt környezetből és titkos névből ) egy titkos kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="4c352-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c352-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4c352-122">-VaultName</span></span>
<span data-ttu-id="4c352-123">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="4c352-123">Vault name.</span></span>
<span data-ttu-id="4c352-124">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="4c352-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4c352-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c352-125">-Confirm</span></span>
<span data-ttu-id="4c352-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4c352-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c352-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c352-127">-WhatIf</span></span>
<span data-ttu-id="4c352-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4c352-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c352-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c352-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c352-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c352-130">CommonParameters</span></span>
<span data-ttu-id="4c352-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c352-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c352-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c352-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c352-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c352-133">INPUTS</span></span>

### <span data-ttu-id="4c352-134">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4c352-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="4c352-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c352-135">OUTPUTS</span></span>

### <span data-ttu-id="4c352-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4c352-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="4c352-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4c352-137">NOTES</span></span>

## <span data-ttu-id="4c352-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c352-138">RELATED LINKS</span></span>

[<span data-ttu-id="4c352-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4c352-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="4c352-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4c352-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="4c352-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4c352-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
