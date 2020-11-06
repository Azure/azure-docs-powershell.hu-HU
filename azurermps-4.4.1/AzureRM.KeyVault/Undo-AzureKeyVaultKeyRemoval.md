---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: df29d88fbac1a8d2dc382522e24ff143cf075573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504084"
---
# <span data-ttu-id="a7c16-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="a7c16-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="a7c16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7c16-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c16-103">A törölt kulcsok aktív állapotba való visszanyerése.</span><span class="sxs-lookup"><span data-stu-id="a7c16-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7c16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7c16-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7c16-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7c16-105">DESCRIPTION</span></span>
<span data-ttu-id="a7c16-106">A **Visszavonás-AzureKeyVaultKeyRemoval** parancsmag visszaállítja a korábban törölt kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="a7c16-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="a7c16-107">A helyreállított kulcs aktív lesz, és az összes normál művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="a7c16-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="a7c16-108">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="a7c16-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="a7c16-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a7c16-109">EXAMPLES</span></span>

### <span data-ttu-id="a7c16-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a7c16-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="a7c16-111">Ez a parancs a korábban törölt "MyKey" kulcsot aktív és használható állapotba fogja állítani.</span><span class="sxs-lookup"><span data-stu-id="a7c16-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="a7c16-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7c16-112">PARAMETERS</span></span>

### <span data-ttu-id="a7c16-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a7c16-113">-Name</span></span>
<span data-ttu-id="a7c16-114">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="a7c16-114">Key name.</span></span>
<span data-ttu-id="a7c16-115">Parancsmag: a kulcs FQDN-je a boltozat neve, az aktuálisan kijelölt környezet és a kulcs neve alapján.</span><span class="sxs-lookup"><span data-stu-id="a7c16-115">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c16-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a7c16-116">-VaultName</span></span>
<span data-ttu-id="a7c16-117">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="a7c16-117">Vault name.</span></span>
<span data-ttu-id="a7c16-118">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="a7c16-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a7c16-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a7c16-119">-Confirm</span></span>
<span data-ttu-id="a7c16-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a7c16-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7c16-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7c16-121">-WhatIf</span></span>
<span data-ttu-id="a7c16-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a7c16-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7c16-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a7c16-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7c16-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7c16-124">-DefaultProfile</span></span>
<span data-ttu-id="a7c16-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7c16-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7c16-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c16-126">CommonParameters</span></span>
<span data-ttu-id="a7c16-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7c16-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c16-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7c16-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c16-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7c16-129">INPUTS</span></span>

### <span data-ttu-id="a7c16-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a7c16-130">System.String</span></span>

## <span data-ttu-id="a7c16-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7c16-131">OUTPUTS</span></span>

### <span data-ttu-id="a7c16-132">Microsoft. Azure. Command. Vault. models. Bundle</span><span class="sxs-lookup"><span data-stu-id="a7c16-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="a7c16-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7c16-133">NOTES</span></span>

## <span data-ttu-id="a7c16-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7c16-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7c16-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a7c16-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="a7c16-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a7c16-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="a7c16-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a7c16-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

