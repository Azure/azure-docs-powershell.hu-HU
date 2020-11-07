---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 57fdddfea449bbde18762afaed0c576c2b4d1db3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679431"
---
# <span data-ttu-id="9ccfd-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="9ccfd-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="9ccfd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ccfd-102">SYNOPSIS</span></span>
<span data-ttu-id="9ccfd-103">Törölt kulcsfájl aktív állapotba való visszanyerése.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ccfd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ccfd-104">SYNTAX</span></span>

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ccfd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ccfd-105">DESCRIPTION</span></span>
<span data-ttu-id="9ccfd-106">A **Visszavonás-AzureRmKeyVaultRemoval** parancsmag egy korábban törölt fő boltozatot fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-106">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="9ccfd-107">A helyreállított boltozat aktívvá válik a helyreállítás után</span><span class="sxs-lookup"><span data-stu-id="9ccfd-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="9ccfd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9ccfd-108">EXAMPLES</span></span>

### <span data-ttu-id="9ccfd-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9ccfd-109">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="9ccfd-110">Ez a parancs helyreállítja a "MyKeyVault" kulcsot, amelyet korábban törölt a eastus2-területről és a "MyResourceGroup" erőforráscsoport nevéből aktív és használható állapotba.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="9ccfd-111">A címkék az új címkét is felváltják.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="9ccfd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ccfd-112">PARAMETERS</span></span>

### <span data-ttu-id="9ccfd-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="9ccfd-113">-Location</span></span>
<span data-ttu-id="9ccfd-114">A törölt Vault eredeti Azure-területét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-114">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ccfd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ccfd-115">-ResourceGroupName</span></span>
<span data-ttu-id="9ccfd-116">Annak a meglévő erőforrás-csoportnak a nevét adja meg, amelybe a kulcs boltozatát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-116">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ccfd-117">-Címke</span><span class="sxs-lookup"><span data-stu-id="9ccfd-117">-Tag</span></span>
<span data-ttu-id="9ccfd-118">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9ccfd-119">Példa:</span><span class="sxs-lookup"><span data-stu-id="9ccfd-119">For example:</span></span>

<span data-ttu-id="9ccfd-120">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="9ccfd-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ccfd-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9ccfd-121">-VaultName</span></span>
<span data-ttu-id="9ccfd-122">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-122">Vault name.</span></span>
<span data-ttu-id="9ccfd-123">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ccfd-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9ccfd-124">-Confirm</span></span>
<span data-ttu-id="9ccfd-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ccfd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ccfd-126">-WhatIf</span></span>
<span data-ttu-id="9ccfd-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ccfd-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ccfd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ccfd-129">-DefaultProfile</span></span>
<span data-ttu-id="9ccfd-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ccfd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ccfd-131">CommonParameters</span></span>
<span data-ttu-id="9ccfd-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ccfd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ccfd-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ccfd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ccfd-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ccfd-134">INPUTS</span></span>

### <span data-ttu-id="9ccfd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9ccfd-135">System.String</span></span>
<span data-ttu-id="9ccfd-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9ccfd-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9ccfd-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ccfd-137">OUTPUTS</span></span>

### <span data-ttu-id="9ccfd-138">Microsoft. Azure. Command. PSVault. models.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="9ccfd-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ccfd-139">NOTES</span></span>

## <span data-ttu-id="9ccfd-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ccfd-140">RELATED LINKS</span></span>

[<span data-ttu-id="9ccfd-141">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9ccfd-141">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="9ccfd-142">Új – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9ccfd-142">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="9ccfd-143">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9ccfd-143">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
