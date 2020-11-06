---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 94e1b297879e31ff42f9c12c0e4ad4a601e5e163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501808"
---
# <span data-ttu-id="03e61-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="03e61-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="03e61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03e61-102">SYNOPSIS</span></span>
<span data-ttu-id="03e61-103">Újragenerálja a Key Vault Managed Azure Storage-fiók megadott kulcsát.</span><span class="sxs-lookup"><span data-stu-id="03e61-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03e61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03e61-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03e61-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03e61-105">DESCRIPTION</span></span>
<span data-ttu-id="03e61-106">Újragenerálja a Key Vault Managed Azure Storage fiók megadott kulcsát, és az aktív kulcsként állítja be a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="03e61-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="03e61-107">A kulcsfájl az Azure Resource Manager hívásával hozza létre újra a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="03e61-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="03e61-108">A hívónak rendelkeznie kell engedélyekkel a megadott Azure-tárterületen lévő kulcsok újragenerálásához.</span><span class="sxs-lookup"><span data-stu-id="03e61-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="03e61-109">Példák</span><span class="sxs-lookup"><span data-stu-id="03e61-109">EXAMPLES</span></span>

### <span data-ttu-id="03e61-110">1. példa: kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="03e61-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="03e61-111">Újragenerálja a "mystorageaccount" key1, és a "key1" értéket állítja be a Key Vault Managed Azure tárterület-fiókjának aktív állapotában.</span><span class="sxs-lookup"><span data-stu-id="03e61-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="03e61-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03e61-112">PARAMETERS</span></span>

### <span data-ttu-id="03e61-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="03e61-113">-AccountName</span></span>
<span data-ttu-id="03e61-114">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="03e61-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="03e61-115">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="03e61-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e61-116">-Force</span><span class="sxs-lookup"><span data-stu-id="03e61-116">-Force</span></span>
<span data-ttu-id="03e61-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03e61-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e61-118">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="03e61-118">-KeyName</span></span>
<span data-ttu-id="03e61-119">A tárolási fiók kulcsának neve az újrageneráláshoz és az aktív állapotba tételéhez.</span><span class="sxs-lookup"><span data-stu-id="03e61-119">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e61-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03e61-120">-PassThru</span></span>
<span data-ttu-id="03e61-121">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="03e61-121">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="03e61-122">Ha meg van adva ez a kapcsoló, akkor a parancsmag a törölt tárterület-fiókot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="03e61-122">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e61-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="03e61-123">-VaultName</span></span>
<span data-ttu-id="03e61-124">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="03e61-124">Vault name.</span></span>
<span data-ttu-id="03e61-125">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="03e61-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="03e61-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="03e61-126">-Confirm</span></span>
<span data-ttu-id="03e61-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03e61-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03e61-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03e61-128">-WhatIf</span></span>
<span data-ttu-id="03e61-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="03e61-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03e61-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03e61-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03e61-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e61-131">-DefaultProfile</span></span>
<span data-ttu-id="03e61-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03e61-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03e61-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e61-133">CommonParameters</span></span>
<span data-ttu-id="03e61-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03e61-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e61-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03e61-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e61-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03e61-136">INPUTS</span></span>

### <span data-ttu-id="03e61-137">System. String</span><span class="sxs-lookup"><span data-stu-id="03e61-137">System.String</span></span>

## <span data-ttu-id="03e61-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03e61-138">OUTPUTS</span></span>

### <span data-ttu-id="03e61-139">Microsoft. Azure. Command. ManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="03e61-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="03e61-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03e61-140">NOTES</span></span>

## <span data-ttu-id="03e61-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03e61-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

