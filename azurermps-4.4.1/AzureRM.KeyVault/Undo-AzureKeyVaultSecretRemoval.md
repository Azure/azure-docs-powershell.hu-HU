---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: e71fa3098003f6fb713c90903eee6e97ca4f42ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679432"
---
# <span data-ttu-id="b3094-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="b3094-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="b3094-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3094-102">SYNOPSIS</span></span>
<span data-ttu-id="b3094-103">Visszanyeri a törölt titkot egy fő boltozatba egy aktív állapotba.</span><span class="sxs-lookup"><span data-stu-id="b3094-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3094-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3094-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3094-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3094-105">DESCRIPTION</span></span>
<span data-ttu-id="b3094-106">A **Visszavonás-AzureKeyVaultSecretRemoval** parancsmag egy korábban törölt titkot fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="b3094-106">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="b3094-107">A helyreállított titok aktív lesz, és minden normális titkos művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="b3094-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="b3094-108">A művelet végrehajtásához a hívónak "vissza" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="b3094-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="b3094-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b3094-109">EXAMPLES</span></span>

### <span data-ttu-id="b3094-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b3094-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="b3094-111">Ez a parancs a korábban törölt titkos "keresési kifejezésként" aktív és felhasználható állapotba helyezi.</span><span class="sxs-lookup"><span data-stu-id="b3094-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="b3094-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3094-112">PARAMETERS</span></span>

### <span data-ttu-id="b3094-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b3094-113">-Name</span></span>
<span data-ttu-id="b3094-114">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="b3094-114">Secret name.</span></span>
<span data-ttu-id="b3094-115">A parancsmag a boltozat nevéből, az aktuálisan kijelölt környezetből és a titkos névvel elkészíti a titkos FQDN-t.</span><span class="sxs-lookup"><span data-stu-id="b3094-115">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3094-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b3094-116">-VaultName</span></span>
<span data-ttu-id="b3094-117">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="b3094-117">Vault name.</span></span>
<span data-ttu-id="b3094-118">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="b3094-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b3094-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b3094-119">-Confirm</span></span>
<span data-ttu-id="b3094-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b3094-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3094-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3094-121">-WhatIf</span></span>
<span data-ttu-id="b3094-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b3094-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3094-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3094-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3094-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3094-124">-DefaultProfile</span></span>
<span data-ttu-id="b3094-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3094-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3094-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3094-126">CommonParameters</span></span>
<span data-ttu-id="b3094-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3094-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3094-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3094-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3094-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3094-129">INPUTS</span></span>

### <span data-ttu-id="b3094-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b3094-130">System.String</span></span>

## <span data-ttu-id="b3094-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3094-131">OUTPUTS</span></span>

### <span data-ttu-id="b3094-132">Microsoft. Azure. Command. kulccsal. modellek. Secret</span><span class="sxs-lookup"><span data-stu-id="b3094-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="b3094-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3094-133">NOTES</span></span>

## <span data-ttu-id="b3094-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3094-134">RELATED LINKS</span></span>

[<span data-ttu-id="b3094-135">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b3094-135">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="b3094-136">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b3094-136">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="b3094-137">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b3094-137">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
