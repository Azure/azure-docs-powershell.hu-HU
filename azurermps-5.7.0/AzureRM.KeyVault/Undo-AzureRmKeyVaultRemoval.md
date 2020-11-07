---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 83737a7643c78ef4ec41d84e153690b3a53a8d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680159"
---
# <span data-ttu-id="9c96b-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="9c96b-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="9c96b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c96b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c96b-103">Törölt kulcsfájl aktív állapotba való visszanyerése.</span><span class="sxs-lookup"><span data-stu-id="9c96b-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c96b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c96b-104">SYNTAX</span></span>

### <span data-ttu-id="9c96b-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c96b-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c96b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9c96b-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-ResourceGroupName] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c96b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c96b-107">DESCRIPTION</span></span>
<span data-ttu-id="9c96b-108">A **Visszavonás-AzureRmKeyVaultRemoval** parancsmag egy korábban törölt fő boltozatot fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="9c96b-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="9c96b-109">A helyreállított boltozat aktívvá válik a helyreállítás után</span><span class="sxs-lookup"><span data-stu-id="9c96b-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="9c96b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9c96b-110">EXAMPLES</span></span>

### <span data-ttu-id="9c96b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9c96b-111">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="9c96b-112">Ez a parancs helyreállítja a "MyKeyVault" kulcsot, amelyet korábban törölt a eastus2-területről és a "MyResourceGroup" erőforráscsoport nevéből aktív és használható állapotba.</span><span class="sxs-lookup"><span data-stu-id="9c96b-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="9c96b-113">A címkék az új címkét is felváltják.</span><span class="sxs-lookup"><span data-stu-id="9c96b-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="9c96b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c96b-114">PARAMETERS</span></span>

### <span data-ttu-id="9c96b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c96b-115">-DefaultProfile</span></span>
<span data-ttu-id="9c96b-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9c96b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c96b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c96b-117">-InputObject</span></span>
<span data-ttu-id="9c96b-118">A Vault-objektum törlése</span><span class="sxs-lookup"><span data-stu-id="9c96b-118">Deleted vault object</span></span>

```yaml
Type: PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c96b-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="9c96b-119">-Location</span></span>
<span data-ttu-id="9c96b-120">A törölt Vault eredeti Azure-területét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c96b-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c96b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c96b-121">-ResourceGroupName</span></span>
<span data-ttu-id="9c96b-122">Annak a meglévő erőforrás-csoportnak a nevét adja meg, amelybe a kulcs boltozatát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="9c96b-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c96b-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="9c96b-123">-Tag</span></span>
<span data-ttu-id="9c96b-124">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="9c96b-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9c96b-125">Példa:</span><span class="sxs-lookup"><span data-stu-id="9c96b-125">For example:</span></span>

<span data-ttu-id="9c96b-126">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="9c96b-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c96b-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9c96b-127">-VaultName</span></span>
<span data-ttu-id="9c96b-128">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="9c96b-128">Vault name.</span></span>
<span data-ttu-id="9c96b-129">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="9c96b-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c96b-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c96b-130">-Confirm</span></span>
<span data-ttu-id="9c96b-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c96b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c96b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c96b-132">-WhatIf</span></span>
<span data-ttu-id="9c96b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c96b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c96b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c96b-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c96b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c96b-135">CommonParameters</span></span>
<span data-ttu-id="9c96b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c96b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c96b-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c96b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c96b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c96b-138">INPUTS</span></span>

### <span data-ttu-id="9c96b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9c96b-139">System.String</span></span>
<span data-ttu-id="9c96b-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9c96b-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9c96b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c96b-141">OUTPUTS</span></span>

### <span data-ttu-id="9c96b-142">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="9c96b-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="9c96b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c96b-143">NOTES</span></span>

## <span data-ttu-id="9c96b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c96b-144">RELATED LINKS</span></span>

[<span data-ttu-id="9c96b-145">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9c96b-145">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="9c96b-146">Új – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9c96b-146">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="9c96b-147">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9c96b-147">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
