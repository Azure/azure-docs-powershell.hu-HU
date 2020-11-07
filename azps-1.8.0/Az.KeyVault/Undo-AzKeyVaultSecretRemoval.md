---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 26bf7b91b330032e05f96f425cb21908fc3df55d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835618"
---
# <span data-ttu-id="0f081-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="0f081-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="0f081-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f081-102">SYNOPSIS</span></span>
<span data-ttu-id="0f081-103">Visszanyeri a törölt titkot egy fő boltozatba egy aktív állapotba.</span><span class="sxs-lookup"><span data-stu-id="0f081-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="0f081-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f081-104">SYNTAX</span></span>

### <span data-ttu-id="0f081-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f081-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f081-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0f081-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f081-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f081-107">DESCRIPTION</span></span>
<span data-ttu-id="0f081-108">A **Visszavonás-AzKeyVaultSecretRemoval** parancsmag egy korábban törölt titkot fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="0f081-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="0f081-109">A helyreállított titok aktív lesz, és minden normális titkos művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="0f081-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="0f081-110">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="0f081-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="0f081-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0f081-111">EXAMPLES</span></span>

### <span data-ttu-id="0f081-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0f081-112">Example 1</span></span>
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

<span data-ttu-id="0f081-113">Ez a parancs a korábban törölt titkos "keresési kifejezésként" aktív és felhasználható állapotba helyezi.</span><span class="sxs-lookup"><span data-stu-id="0f081-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="0f081-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f081-114">PARAMETERS</span></span>

### <span data-ttu-id="0f081-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f081-115">-DefaultProfile</span></span>
<span data-ttu-id="0f081-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0f081-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f081-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f081-117">-InputObject</span></span>
<span data-ttu-id="0f081-118">Titkos objektum törölve</span><span class="sxs-lookup"><span data-stu-id="0f081-118">Deleted secret object</span></span>

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

### <span data-ttu-id="0f081-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f081-119">-Name</span></span>
<span data-ttu-id="0f081-120">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="0f081-120">Secret name.</span></span>
<span data-ttu-id="0f081-121">A parancsmag a boltozat nevéből, az aktuálisan kijelölt környezetből és a titkos névvel elkészíti a titkos FQDN-t.</span><span class="sxs-lookup"><span data-stu-id="0f081-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="0f081-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0f081-122">-VaultName</span></span>
<span data-ttu-id="0f081-123">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="0f081-123">Vault name.</span></span>
<span data-ttu-id="0f081-124">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="0f081-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="0f081-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f081-125">-Confirm</span></span>
<span data-ttu-id="0f081-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f081-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f081-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f081-127">-WhatIf</span></span>
<span data-ttu-id="0f081-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f081-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f081-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f081-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f081-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f081-130">CommonParameters</span></span>
<span data-ttu-id="0f081-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f081-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f081-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f081-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f081-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f081-133">INPUTS</span></span>

### <span data-ttu-id="0f081-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0f081-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="0f081-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f081-135">OUTPUTS</span></span>

### <span data-ttu-id="0f081-136">Microsoft. Azure. Command. PSKeyVaultSecret. models.</span><span class="sxs-lookup"><span data-stu-id="0f081-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="0f081-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f081-137">NOTES</span></span>

## <span data-ttu-id="0f081-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f081-138">RELATED LINKS</span></span>

[<span data-ttu-id="0f081-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0f081-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="0f081-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0f081-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="0f081-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0f081-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
