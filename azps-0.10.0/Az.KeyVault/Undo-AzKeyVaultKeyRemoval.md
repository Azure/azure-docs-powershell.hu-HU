---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: 5b0e67fbbead536803dba8efeb2c8a61d7f75c5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843845"
---
# <span data-ttu-id="1e795-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="1e795-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="1e795-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e795-102">SYNOPSIS</span></span>
<span data-ttu-id="1e795-103">A törölt kulcsok aktív állapotba való visszanyerése.</span><span class="sxs-lookup"><span data-stu-id="1e795-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="1e795-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e795-104">SYNTAX</span></span>

```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e795-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e795-105">DESCRIPTION</span></span>
<span data-ttu-id="1e795-106">A **Visszavonás-AzKeyVaultKeyRemoval** parancsmag visszaállítja a korábban törölt kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="1e795-106">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="1e795-107">A helyreállított kulcs aktív lesz, és az összes normál művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="1e795-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="1e795-108">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="1e795-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="1e795-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1e795-109">EXAMPLES</span></span>

### <span data-ttu-id="1e795-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1e795-110">Example 1</span></span>
```
PS C:\>Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="1e795-111">Ez a parancs a korábban törölt "MyKey" kulcsot aktív és használható állapotba fogja állítani.</span><span class="sxs-lookup"><span data-stu-id="1e795-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="1e795-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e795-112">PARAMETERS</span></span>

### <span data-ttu-id="1e795-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e795-113">-DefaultProfile</span></span>
<span data-ttu-id="1e795-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1e795-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e795-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e795-115">-Name</span></span>
<span data-ttu-id="1e795-116">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="1e795-116">Key name.</span></span>
<span data-ttu-id="1e795-117">Parancsmag: a kulcs FQDN-je a boltozat neve, az aktuálisan kijelölt környezet és a kulcs neve alapján.</span><span class="sxs-lookup"><span data-stu-id="1e795-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="1e795-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1e795-118">-VaultName</span></span>
<span data-ttu-id="1e795-119">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="1e795-119">Vault name.</span></span>
<span data-ttu-id="1e795-120">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="1e795-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1e795-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e795-121">-Confirm</span></span>
<span data-ttu-id="1e795-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e795-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e795-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e795-123">-WhatIf</span></span>
<span data-ttu-id="1e795-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1e795-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e795-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e795-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e795-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e795-126">CommonParameters</span></span>
<span data-ttu-id="1e795-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e795-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e795-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e795-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e795-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e795-129">INPUTS</span></span>

### <span data-ttu-id="1e795-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1e795-130">System.String</span></span>

## <span data-ttu-id="1e795-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e795-131">OUTPUTS</span></span>

### <span data-ttu-id="1e795-132">Microsoft. Azure. Command. Vault. models. Bundle</span><span class="sxs-lookup"><span data-stu-id="1e795-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="1e795-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e795-133">NOTES</span></span>

## <span data-ttu-id="1e795-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e795-134">RELATED LINKS</span></span>

[<span data-ttu-id="1e795-135">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e795-135">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="1e795-136">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e795-136">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="1e795-137">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e795-137">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

