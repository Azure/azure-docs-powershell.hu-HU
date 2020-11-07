---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: e65bef4119c51b989287bbf0db2e7587fef50271
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843834"
---
# <span data-ttu-id="17e63-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="17e63-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="17e63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17e63-102">SYNOPSIS</span></span>
<span data-ttu-id="17e63-103">Visszanyeri a törölt titkot egy fő boltozatba egy aktív állapotba.</span><span class="sxs-lookup"><span data-stu-id="17e63-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="17e63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17e63-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17e63-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="17e63-105">DESCRIPTION</span></span>
<span data-ttu-id="17e63-106">A **Visszavonás-AzKeyVaultSecretRemoval** parancsmag egy korábban törölt titkot fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="17e63-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="17e63-107">A helyreállított titok aktív lesz, és minden normális titkos művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="17e63-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="17e63-108">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="17e63-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="17e63-109">Példák</span><span class="sxs-lookup"><span data-stu-id="17e63-109">EXAMPLES</span></span>

### <span data-ttu-id="17e63-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="17e63-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="17e63-111">Ez a parancs a korábban törölt titkos "keresési kifejezésként" aktív és felhasználható állapotba helyezi.</span><span class="sxs-lookup"><span data-stu-id="17e63-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="17e63-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17e63-112">PARAMETERS</span></span>

### <span data-ttu-id="17e63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e63-113">-DefaultProfile</span></span>
<span data-ttu-id="17e63-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="17e63-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17e63-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17e63-115">-Name</span></span>
<span data-ttu-id="17e63-116">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="17e63-116">Secret name.</span></span>
<span data-ttu-id="17e63-117">A parancsmag a boltozat nevéből, az aktuálisan kijelölt környezetből és a titkos névvel elkészíti a titkos FQDN-t.</span><span class="sxs-lookup"><span data-stu-id="17e63-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e63-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="17e63-118">-VaultName</span></span>
<span data-ttu-id="17e63-119">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="17e63-119">Vault name.</span></span>
<span data-ttu-id="17e63-120">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="17e63-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="17e63-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="17e63-121">-Confirm</span></span>
<span data-ttu-id="17e63-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="17e63-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17e63-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17e63-123">-WhatIf</span></span>
<span data-ttu-id="17e63-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="17e63-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17e63-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17e63-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17e63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e63-126">CommonParameters</span></span>
<span data-ttu-id="17e63-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17e63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e63-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17e63-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e63-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17e63-129">INPUTS</span></span>

### <span data-ttu-id="17e63-130">System. String</span><span class="sxs-lookup"><span data-stu-id="17e63-130">System.String</span></span>

## <span data-ttu-id="17e63-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17e63-131">OUTPUTS</span></span>

### <span data-ttu-id="17e63-132">Microsoft. Azure. Command. kulccsal. modellek. Secret</span><span class="sxs-lookup"><span data-stu-id="17e63-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="17e63-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17e63-133">NOTES</span></span>

## <span data-ttu-id="17e63-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17e63-134">RELATED LINKS</span></span>

[<span data-ttu-id="17e63-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17e63-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="17e63-136">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17e63-136">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="17e63-137">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17e63-137">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
