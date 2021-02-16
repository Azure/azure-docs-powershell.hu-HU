---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9c240d3902aeba38af4281ba31bacea76bad0a58
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399090"
---
# <span data-ttu-id="2ec25-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="2ec25-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="2ec25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ec25-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec25-103">Egy kulcstár törölt titkos kulcsát aktív állapotba helyreállítja.</span><span class="sxs-lookup"><span data-stu-id="2ec25-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="2ec25-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2ec25-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ec25-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2ec25-105">DESCRIPTION</span></span>
<span data-ttu-id="2ec25-106">Az **Undo-AzKeyVaultSecretRemoval** parancsmag helyreállít egy korábban törölt titkos adatokat.</span><span class="sxs-lookup"><span data-stu-id="2ec25-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="2ec25-107">A helyreállított titkos titkos művelet aktív lesz, és minden normál titkos művelethez használható.</span><span class="sxs-lookup"><span data-stu-id="2ec25-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="2ec25-108">A művelet végrehajtásához a hívónak "helyreállítás" engedéllyel kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="2ec25-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="2ec25-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2ec25-109">EXAMPLES</span></span>

### <span data-ttu-id="2ec25-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="2ec25-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="2ec25-111">Ez a parancs egy aktív és használható állapotba visszaállítja a korábban törölt MySecret titkos fájlt.</span><span class="sxs-lookup"><span data-stu-id="2ec25-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="2ec25-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ec25-112">PARAMETERS</span></span>

### <span data-ttu-id="2ec25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec25-113">-DefaultProfile</span></span>
<span data-ttu-id="2ec25-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2ec25-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ec25-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2ec25-115">-Name</span></span>
<span data-ttu-id="2ec25-116">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="2ec25-116">Secret name.</span></span>
<span data-ttu-id="2ec25-117">A parancsmag a tárolónévből ( jelenleg kijelölt környezetből és titkos névből ) egy titkos kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="2ec25-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="2ec25-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2ec25-118">-VaultName</span></span>
<span data-ttu-id="2ec25-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="2ec25-119">Vault name.</span></span>
<span data-ttu-id="2ec25-120">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="2ec25-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2ec25-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ec25-121">-Confirm</span></span>
<span data-ttu-id="2ec25-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2ec25-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ec25-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ec25-123">-WhatIf</span></span>
<span data-ttu-id="2ec25-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2ec25-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ec25-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ec25-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ec25-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec25-126">CommonParameters</span></span>
<span data-ttu-id="2ec25-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec25-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec25-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec25-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec25-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ec25-129">INPUTS</span></span>

### <span data-ttu-id="2ec25-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2ec25-130">System.String</span></span>

## <span data-ttu-id="2ec25-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ec25-131">OUTPUTS</span></span>

### <span data-ttu-id="2ec25-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span><span class="sxs-lookup"><span data-stu-id="2ec25-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="2ec25-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2ec25-133">NOTES</span></span>

## <span data-ttu-id="2ec25-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ec25-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ec25-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2ec25-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="2ec25-136">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2ec25-136">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
