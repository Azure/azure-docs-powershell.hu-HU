---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 317a7f72e68f442608a0b163afd99af6eaac28c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494472"
---
# <span data-ttu-id="f0717-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f0717-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="f0717-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0717-102">SYNOPSIS</span></span>
<span data-ttu-id="f0717-103">Újragenerálja a Key Vault Managed Azure Storage-fiók megadott kulcsát.</span><span class="sxs-lookup"><span data-stu-id="f0717-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0717-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0717-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0717-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0717-105">DESCRIPTION</span></span>
<span data-ttu-id="f0717-106">Újragenerálja a Key Vault Managed Azure Storage fiók megadott kulcsát, és az aktív kulcsként állítja be a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="f0717-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="f0717-107">A kulcsfájl az Azure Resource Manager hívásával hozza létre újra a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="f0717-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="f0717-108">A hívónak rendelkeznie kell engedélyekkel a megadott Azure-tárterületen lévő kulcsok újragenerálásához.</span><span class="sxs-lookup"><span data-stu-id="f0717-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="f0717-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f0717-109">EXAMPLES</span></span>

### <span data-ttu-id="f0717-110">1. példa: kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="f0717-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="f0717-111">Újragenerálja a "mystorageaccount" key1, és a "key1" értéket állítja be a Key Vault Managed Azure tárterület-fiókjának aktív állapotában.</span><span class="sxs-lookup"><span data-stu-id="f0717-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="f0717-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0717-112">PARAMETERS</span></span>

### <span data-ttu-id="f0717-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f0717-113">-AccountName</span></span>
<span data-ttu-id="f0717-114">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f0717-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="f0717-115">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="f0717-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0717-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0717-116">-DefaultProfile</span></span>
<span data-ttu-id="f0717-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f0717-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0717-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f0717-118">-Force</span></span>
<span data-ttu-id="f0717-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f0717-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0717-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="f0717-120">-KeyName</span></span>
<span data-ttu-id="f0717-121">A tárolási fiók kulcsának neve az újrageneráláshoz és az aktív állapotba tételéhez.</span><span class="sxs-lookup"><span data-stu-id="f0717-121">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0717-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0717-122">-PassThru</span></span>
<span data-ttu-id="f0717-123">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="f0717-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f0717-124">Ha meg van adva ez a kapcsoló, akkor a parancsmag a törölt tárterület-fiókot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f0717-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0717-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f0717-125">-VaultName</span></span>
<span data-ttu-id="f0717-126">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="f0717-126">Vault name.</span></span>
<span data-ttu-id="f0717-127">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="f0717-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f0717-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f0717-128">-Confirm</span></span>
<span data-ttu-id="f0717-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f0717-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0717-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0717-130">-WhatIf</span></span>
<span data-ttu-id="f0717-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f0717-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0717-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f0717-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0717-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0717-133">CommonParameters</span></span>
<span data-ttu-id="f0717-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0717-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0717-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0717-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0717-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0717-136">INPUTS</span></span>

### <span data-ttu-id="f0717-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f0717-137">System.String</span></span>

## <span data-ttu-id="f0717-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0717-138">OUTPUTS</span></span>

### <span data-ttu-id="f0717-139">Microsoft. Azure. Command. ManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="f0717-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="f0717-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0717-140">NOTES</span></span>

## <span data-ttu-id="f0717-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0717-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

