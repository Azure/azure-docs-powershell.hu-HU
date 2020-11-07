---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 438d36a5c9081da3124c0ef5ee03c7eb9ad8f634
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848218"
---
# <span data-ttu-id="4014e-101">Remove-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4014e-101">Remove-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="4014e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4014e-102">SYNOPSIS</span></span>
<span data-ttu-id="4014e-103">A felügyelt Azure Storage-fiók és az összes társított biztonsági társítási definíció eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="4014e-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4014e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4014e-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4014e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4014e-105">DESCRIPTION</span></span>
<span data-ttu-id="4014e-106">Az Azure Storage-fiók társítása a Key Vault-ról</span><span class="sxs-lookup"><span data-stu-id="4014e-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="4014e-107">Ez a művelet nem távolítja el az Azure-tárterületet, de eltávolítja a fiók kulcsait az Azure Key Vault által felügyelt fiókból.</span><span class="sxs-lookup"><span data-stu-id="4014e-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="4014e-108">Az összes társított kulcs boltozata: a biztonsági társítások definíciója is törlődik.</span><span class="sxs-lookup"><span data-stu-id="4014e-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="4014e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4014e-109">EXAMPLES</span></span>

### <span data-ttu-id="4014e-110">1. példa: távolítsa el a fontos Vault Managed Azure Storage-fiókot és az összes társított biztonsági társítási definíciót.</span><span class="sxs-lookup"><span data-stu-id="4014e-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="4014e-111">Az Azure-tárterület "mystorageaccount"-fiókjának társítása a Key Vault "myvault", és a kulcsfájl leállítása a kulcsok kezeléséről.</span><span class="sxs-lookup"><span data-stu-id="4014e-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="4014e-112">Nem törlődik a "mystorageaccount" fiók.</span><span class="sxs-lookup"><span data-stu-id="4014e-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="4014e-113">A program eltávolítja a fiókkal társított összes fontos boltíves tárolót.</span><span class="sxs-lookup"><span data-stu-id="4014e-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="4014e-114">2. példa: távolítsa el a fontos Vault Managed Azure Storage-fiókot és az összes társított biztonsági társítási definíciót felhasználó megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="4014e-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="4014e-115">Az Azure-tárterület "mystorageaccount"-fiókjának társítása a Key Vault "myvault", és a kulcsfájl leállítása a kulcsok kezeléséről.</span><span class="sxs-lookup"><span data-stu-id="4014e-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="4014e-116">Nem törlődik a "mystorageaccount" fiók.</span><span class="sxs-lookup"><span data-stu-id="4014e-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="4014e-117">A program eltávolítja a fiókkal társított összes fontos boltíves tárolót.</span><span class="sxs-lookup"><span data-stu-id="4014e-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="4014e-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4014e-118">PARAMETERS</span></span>

### <span data-ttu-id="4014e-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4014e-119">-AccountName</span></span>
<span data-ttu-id="4014e-120">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="4014e-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="4014e-121">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="4014e-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="4014e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4014e-122">-DefaultProfile</span></span>
<span data-ttu-id="4014e-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4014e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4014e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4014e-124">-Force</span></span>
<span data-ttu-id="4014e-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4014e-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4014e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4014e-126">-PassThru</span></span>
<span data-ttu-id="4014e-127">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="4014e-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4014e-128">Ha meg van adva ez a kapcsoló, akkor a parancsmag a törölt tárterület-fiókot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4014e-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="4014e-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4014e-129">-VaultName</span></span>
<span data-ttu-id="4014e-130">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="4014e-130">Vault name.</span></span>
<span data-ttu-id="4014e-131">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="4014e-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4014e-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4014e-132">-Confirm</span></span>
<span data-ttu-id="4014e-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4014e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4014e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4014e-134">-WhatIf</span></span>
<span data-ttu-id="4014e-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4014e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4014e-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4014e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4014e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4014e-137">CommonParameters</span></span>
<span data-ttu-id="4014e-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4014e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4014e-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4014e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4014e-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4014e-140">INPUTS</span></span>

### <span data-ttu-id="4014e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4014e-141">System.String</span></span>

## <span data-ttu-id="4014e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4014e-142">OUTPUTS</span></span>

### <span data-ttu-id="4014e-143">Microsoft. Azure. Command. ManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="4014e-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="4014e-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4014e-144">NOTES</span></span>

## <span data-ttu-id="4014e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4014e-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

