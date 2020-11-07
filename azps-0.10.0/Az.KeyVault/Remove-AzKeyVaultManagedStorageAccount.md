---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: d57f672ef440515e69535503f006e08b4c924646
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842101"
---
# <span data-ttu-id="f2d98-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f2d98-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="f2d98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2d98-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d98-103">A felügyelt Azure Storage-fiók és az összes társított biztonsági társítási definíció eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="f2d98-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="f2d98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2d98-104">SYNTAX</span></span>

```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2d98-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2d98-105">DESCRIPTION</span></span>
<span data-ttu-id="f2d98-106">Az Azure Storage-fiók társítása a Key Vault-ról</span><span class="sxs-lookup"><span data-stu-id="f2d98-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="f2d98-107">Ez a művelet nem távolítja el az Azure-tárterületet, de eltávolítja a fiók kulcsait az Azure Key Vault által felügyelt fiókból.</span><span class="sxs-lookup"><span data-stu-id="f2d98-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="f2d98-108">Az összes társított kulcs boltozata: a biztonsági társítások definíciója is törlődik.</span><span class="sxs-lookup"><span data-stu-id="f2d98-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="f2d98-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f2d98-109">EXAMPLES</span></span>

### <span data-ttu-id="f2d98-110">1. példa: távolítsa el a fontos Vault Managed Azure Storage-fiókot és az összes társított biztonsági társítási definíciót.</span><span class="sxs-lookup"><span data-stu-id="f2d98-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="f2d98-111">Az Azure-tárterület "mystorageaccount"-fiókjának társítása a Key Vault "myvault", és a kulcsfájl leállítása a kulcsok kezeléséről.</span><span class="sxs-lookup"><span data-stu-id="f2d98-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="f2d98-112">Nem törlődik a "mystorageaccount" fiók.</span><span class="sxs-lookup"><span data-stu-id="f2d98-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="f2d98-113">A program eltávolítja a fiókkal társított összes fontos boltíves tárolót.</span><span class="sxs-lookup"><span data-stu-id="f2d98-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="f2d98-114">2. példa: távolítsa el a fontos Vault Managed Azure Storage-fiókot és az összes társított biztonsági társítási definíciót felhasználó megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="f2d98-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="f2d98-115">Az Azure-tárterület "mystorageaccount"-fiókjának társítása a Key Vault "myvault", és a kulcsfájl leállítása a kulcsok kezeléséről.</span><span class="sxs-lookup"><span data-stu-id="f2d98-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="f2d98-116">Nem törlődik a "mystorageaccount" fiók.</span><span class="sxs-lookup"><span data-stu-id="f2d98-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="f2d98-117">A program eltávolítja a fiókkal társított összes fontos boltíves tárolót.</span><span class="sxs-lookup"><span data-stu-id="f2d98-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="f2d98-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2d98-118">PARAMETERS</span></span>

### <span data-ttu-id="f2d98-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2d98-119">-AccountName</span></span>
<span data-ttu-id="f2d98-120">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f2d98-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="f2d98-121">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="f2d98-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="f2d98-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d98-122">-DefaultProfile</span></span>
<span data-ttu-id="f2d98-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f2d98-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2d98-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f2d98-124">-Force</span></span>
<span data-ttu-id="f2d98-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f2d98-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f2d98-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2d98-126">-PassThru</span></span>
<span data-ttu-id="f2d98-127">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="f2d98-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f2d98-128">Ha meg van adva ez a kapcsoló, akkor a parancsmag a törölt tárterület-fiókot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f2d98-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="f2d98-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f2d98-129">-VaultName</span></span>
<span data-ttu-id="f2d98-130">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="f2d98-130">Vault name.</span></span>
<span data-ttu-id="f2d98-131">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="f2d98-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f2d98-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f2d98-132">-Confirm</span></span>
<span data-ttu-id="f2d98-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f2d98-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2d98-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2d98-134">-WhatIf</span></span>
<span data-ttu-id="f2d98-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f2d98-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2d98-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f2d98-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2d98-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d98-137">CommonParameters</span></span>
<span data-ttu-id="f2d98-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2d98-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d98-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2d98-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d98-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2d98-140">INPUTS</span></span>

### <span data-ttu-id="f2d98-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f2d98-141">System.String</span></span>

## <span data-ttu-id="f2d98-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2d98-142">OUTPUTS</span></span>

### <span data-ttu-id="f2d98-143">Microsoft. Azure. Command. ManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="f2d98-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="f2d98-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2d98-144">NOTES</span></span>

## <span data-ttu-id="f2d98-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2d98-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

