---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azmanagedhsmkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
ms.openlocfilehash: be1713584a1d0ce897c1c728f6aa7ae8b6ca3255
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185280"
---
# <span data-ttu-id="f60b0-101">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="f60b0-101">Undo-AzManagedHsmKeyRemoval</span></span>

## <span data-ttu-id="f60b0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f60b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f60b0-103">A kezelt HSM törölt kulcsait aktív állapotba veszi.</span><span class="sxs-lookup"><span data-stu-id="f60b0-103">Recovers a deleted key in a managed HSM into an active state.</span></span>

## <span data-ttu-id="f60b0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f60b0-104">SYNTAX</span></span>

### <span data-ttu-id="f60b0-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f60b0-105">Default (Default)</span></span>
```
Undo-AzManagedHsmKeyRemoval [-HsmName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f60b0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f60b0-106">InputObject</span></span>
```
Undo-AzManagedHsmKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f60b0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f60b0-107">DESCRIPTION</span></span>
<span data-ttu-id="f60b0-108">A **Visszavonás-AzManagedHsmKeyRemoval** parancsmag visszaállítja a korábban törölt kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="f60b0-108">The **Undo-AzManagedHsmKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="f60b0-109">A helyreállított kulcs aktív lesz, és az összes normál művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="f60b0-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="f60b0-110">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="f60b0-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="f60b0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f60b0-111">EXAMPLES</span></span>

### <span data-ttu-id="f60b0-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f60b0-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzManagedHsmKeyRemoval -HsmName testmhsm -Name testkey001

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="f60b0-113">Ez a parancs a korábban törölt "testkey001" kulcsot aktív és használható állapotba fogja állítani.</span><span class="sxs-lookup"><span data-stu-id="f60b0-113">This command will recover the key 'testkey001' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="f60b0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f60b0-114">PARAMETERS</span></span>

### <span data-ttu-id="f60b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60b0-115">-DefaultProfile</span></span>
<span data-ttu-id="f60b0-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f60b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f60b0-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="f60b0-117">-HsmName</span></span>
<span data-ttu-id="f60b0-118">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="f60b0-118">HSM name.</span></span> <span data-ttu-id="f60b0-119">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="f60b0-119">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f60b0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f60b0-120">-InputObject</span></span>
<span data-ttu-id="f60b0-121">Törölt kulcs objektum</span><span class="sxs-lookup"><span data-stu-id="f60b0-121">Deleted key object</span></span>

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

### <span data-ttu-id="f60b0-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f60b0-122">-Name</span></span>
<span data-ttu-id="f60b0-123">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="f60b0-123">Key name.</span></span>
<span data-ttu-id="f60b0-124">Parancsmag: a felügyelt HSM-név, az aktuálisan kijelölt környezet és a kulcsnév alapján egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="f60b0-124">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="f60b0-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f60b0-125">-Confirm</span></span>
<span data-ttu-id="f60b0-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f60b0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f60b0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f60b0-127">-WhatIf</span></span>
<span data-ttu-id="f60b0-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f60b0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f60b0-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f60b0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f60b0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60b0-130">CommonParameters</span></span>
<span data-ttu-id="f60b0-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f60b0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60b0-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f60b0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60b0-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f60b0-133">INPUTS</span></span>

### <span data-ttu-id="f60b0-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f60b0-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="f60b0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f60b0-135">OUTPUTS</span></span>

### <span data-ttu-id="f60b0-136">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="f60b0-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="f60b0-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f60b0-137">NOTES</span></span>

## <span data-ttu-id="f60b0-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f60b0-138">RELATED LINKS</span></span>

[<span data-ttu-id="f60b0-139">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f60b0-139">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="f60b0-140">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f60b0-140">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="f60b0-141">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f60b0-141">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="f60b0-142">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f60b0-142">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)

[<span data-ttu-id="f60b0-143">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f60b0-143">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="f60b0-144">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f60b0-144">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)