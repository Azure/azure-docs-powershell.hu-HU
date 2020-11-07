---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: fd2483925e8ab14772a3bf34d4411748583a03c9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842085"
---
# <span data-ttu-id="5e03b-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="5e03b-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="5e03b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e03b-102">SYNOPSIS</span></span>
<span data-ttu-id="5e03b-103">Törölt kulcsfájl aktív állapotba való visszanyerése.</span><span class="sxs-lookup"><span data-stu-id="5e03b-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="5e03b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e03b-104">SYNTAX</span></span>

```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e03b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e03b-105">DESCRIPTION</span></span>
<span data-ttu-id="5e03b-106">A **Visszavonás-AzKeyVaultRemoval** parancsmag egy korábban törölt fő boltozatot fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="5e03b-106">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="5e03b-107">A helyreállított boltozat aktívvá válik a helyreállítás után</span><span class="sxs-lookup"><span data-stu-id="5e03b-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="5e03b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5e03b-108">EXAMPLES</span></span>

### <span data-ttu-id="5e03b-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5e03b-109">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="5e03b-110">Ez a parancs helyreállítja a "MyKeyVault" kulcsot, amelyet korábban törölt a eastus2-területről és a "MyResourceGroup" erőforráscsoport nevéből aktív és használható állapotba.</span><span class="sxs-lookup"><span data-stu-id="5e03b-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="5e03b-111">A címkék az új címkét is felváltják.</span><span class="sxs-lookup"><span data-stu-id="5e03b-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="5e03b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e03b-112">PARAMETERS</span></span>

### <span data-ttu-id="5e03b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e03b-113">-DefaultProfile</span></span>
<span data-ttu-id="5e03b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5e03b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e03b-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="5e03b-115">-Location</span></span>
<span data-ttu-id="5e03b-116">A törölt Vault eredeti Azure-területét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e03b-116">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e03b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e03b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e03b-118">Annak a meglévő erőforrás-csoportnak a nevét adja meg, amelybe a kulcs boltozatát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="5e03b-118">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="5e03b-119">-Címke</span><span class="sxs-lookup"><span data-stu-id="5e03b-119">-Tag</span></span>
<span data-ttu-id="5e03b-120">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="5e03b-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5e03b-121">Példa:</span><span class="sxs-lookup"><span data-stu-id="5e03b-121">For example:</span></span>

<span data-ttu-id="5e03b-122">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="5e03b-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5e03b-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5e03b-123">-VaultName</span></span>
<span data-ttu-id="5e03b-124">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="5e03b-124">Vault name.</span></span>
<span data-ttu-id="5e03b-125">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="5e03b-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e03b-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5e03b-126">-Confirm</span></span>
<span data-ttu-id="5e03b-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5e03b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e03b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e03b-128">-WhatIf</span></span>
<span data-ttu-id="5e03b-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5e03b-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e03b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e03b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e03b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e03b-131">CommonParameters</span></span>
<span data-ttu-id="5e03b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e03b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e03b-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e03b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e03b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e03b-134">INPUTS</span></span>

### <span data-ttu-id="5e03b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5e03b-135">System.String</span></span>
<span data-ttu-id="5e03b-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5e03b-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5e03b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e03b-137">OUTPUTS</span></span>

### <span data-ttu-id="5e03b-138">Microsoft. Azure. Command. PSVault. models.</span><span class="sxs-lookup"><span data-stu-id="5e03b-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="5e03b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e03b-139">NOTES</span></span>

## <span data-ttu-id="5e03b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e03b-140">RELATED LINKS</span></span>

[<span data-ttu-id="5e03b-141">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="5e03b-141">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="5e03b-142">Új – AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="5e03b-142">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="5e03b-143">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="5e03b-143">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
