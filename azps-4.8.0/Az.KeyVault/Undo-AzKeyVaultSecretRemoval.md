---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 1eca5a380dc71a5bd801c21bb7e7f556fcff0d35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025298"
---
# <span data-ttu-id="b236f-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="b236f-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="b236f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b236f-102">SYNOPSIS</span></span>
<span data-ttu-id="b236f-103">Visszanyeri a törölt titkot egy fő boltozatba egy aktív állapotba.</span><span class="sxs-lookup"><span data-stu-id="b236f-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="b236f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b236f-104">SYNTAX</span></span>

### <span data-ttu-id="b236f-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b236f-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b236f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b236f-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b236f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b236f-107">DESCRIPTION</span></span>
<span data-ttu-id="b236f-108">A **Visszavonás-AzKeyVaultSecretRemoval** parancsmag egy korábban törölt titkot fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="b236f-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="b236f-109">A helyreállított titok aktív lesz, és minden normális titkos művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="b236f-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="b236f-110">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="b236f-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="b236f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b236f-111">EXAMPLES</span></span>

### <span data-ttu-id="b236f-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b236f-112">Example 1</span></span>
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

<span data-ttu-id="b236f-113">Ez a parancs a korábban törölt titkos "keresési kifejezésként" aktív és felhasználható állapotba helyezi.</span><span class="sxs-lookup"><span data-stu-id="b236f-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="b236f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b236f-114">PARAMETERS</span></span>

### <span data-ttu-id="b236f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b236f-115">-DefaultProfile</span></span>
<span data-ttu-id="b236f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b236f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b236f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b236f-117">-InputObject</span></span>
<span data-ttu-id="b236f-118">Titkos objektum törölve</span><span class="sxs-lookup"><span data-stu-id="b236f-118">Deleted secret object</span></span>

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

### <span data-ttu-id="b236f-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b236f-119">-Name</span></span>
<span data-ttu-id="b236f-120">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="b236f-120">Secret name.</span></span>
<span data-ttu-id="b236f-121">A parancsmag a boltozat nevéből, az aktuálisan kijelölt környezetből és a titkos névvel elkészíti a titkos FQDN-t.</span><span class="sxs-lookup"><span data-stu-id="b236f-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="b236f-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b236f-122">-VaultName</span></span>
<span data-ttu-id="b236f-123">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="b236f-123">Vault name.</span></span>
<span data-ttu-id="b236f-124">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="b236f-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b236f-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b236f-125">-Confirm</span></span>
<span data-ttu-id="b236f-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b236f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b236f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b236f-127">-WhatIf</span></span>
<span data-ttu-id="b236f-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b236f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b236f-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b236f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b236f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b236f-130">CommonParameters</span></span>
<span data-ttu-id="b236f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b236f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b236f-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b236f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b236f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b236f-133">INPUTS</span></span>

### <span data-ttu-id="b236f-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b236f-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="b236f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b236f-135">OUTPUTS</span></span>

### <span data-ttu-id="b236f-136">Microsoft. Azure. Command. PSKeyVaultSecret. models.</span><span class="sxs-lookup"><span data-stu-id="b236f-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="b236f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b236f-137">NOTES</span></span>

## <span data-ttu-id="b236f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b236f-138">RELATED LINKS</span></span>

[<span data-ttu-id="b236f-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b236f-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="b236f-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b236f-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="b236f-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b236f-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
