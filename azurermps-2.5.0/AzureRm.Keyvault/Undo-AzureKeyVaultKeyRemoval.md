---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
ms.openlocfilehash: 831bcdb76a0f24a2935f2ffd2ed0bf7df1c10042
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849290"
---
# <span data-ttu-id="8fb26-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="8fb26-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="8fb26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fb26-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb26-103">A törölt kulcsok aktív állapotba való visszanyerése.</span><span class="sxs-lookup"><span data-stu-id="8fb26-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fb26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fb26-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fb26-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fb26-105">DESCRIPTION</span></span>
<span data-ttu-id="8fb26-106">A **Visszavonás-AzureKeyVaultKeyRemoval** parancsmag visszaállítja a korábban törölt kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="8fb26-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="8fb26-107">A helyreállított kulcs aktív lesz, és az összes normál művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="8fb26-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="8fb26-108">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="8fb26-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="8fb26-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8fb26-109">EXAMPLES</span></span>

### <span data-ttu-id="8fb26-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8fb26-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="8fb26-111">Ez a parancs a korábban törölt "MyKey" kulcsot aktív és használható állapotba fogja állítani.</span><span class="sxs-lookup"><span data-stu-id="8fb26-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="8fb26-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fb26-112">PARAMETERS</span></span>

### <span data-ttu-id="8fb26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb26-113">-DefaultProfile</span></span>
<span data-ttu-id="8fb26-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8fb26-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fb26-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8fb26-115">-Name</span></span>
<span data-ttu-id="8fb26-116">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="8fb26-116">Key name.</span></span>
<span data-ttu-id="8fb26-117">Parancsmag: a kulcs FQDN-je a boltozat neve, az aktuálisan kijelölt környezet és a kulcs neve alapján.</span><span class="sxs-lookup"><span data-stu-id="8fb26-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb26-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8fb26-118">-VaultName</span></span>
<span data-ttu-id="8fb26-119">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="8fb26-119">Vault name.</span></span>
<span data-ttu-id="8fb26-120">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="8fb26-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8fb26-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8fb26-121">-Confirm</span></span>
<span data-ttu-id="8fb26-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8fb26-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fb26-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fb26-123">-WhatIf</span></span>
<span data-ttu-id="8fb26-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8fb26-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fb26-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8fb26-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fb26-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb26-126">CommonParameters</span></span>
<span data-ttu-id="8fb26-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fb26-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb26-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fb26-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb26-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fb26-129">INPUTS</span></span>

### <span data-ttu-id="8fb26-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8fb26-130">System.String</span></span>

## <span data-ttu-id="8fb26-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fb26-131">OUTPUTS</span></span>

### <span data-ttu-id="8fb26-132">Microsoft. Azure. Command. Vault. models. Bundle</span><span class="sxs-lookup"><span data-stu-id="8fb26-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="8fb26-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fb26-133">NOTES</span></span>

## <span data-ttu-id="8fb26-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fb26-134">RELATED LINKS</span></span>

[<span data-ttu-id="8fb26-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8fb26-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="8fb26-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8fb26-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="8fb26-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8fb26-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

