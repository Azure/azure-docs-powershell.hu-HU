---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 51e7b941e5dbb4d07b48444196f6e3d3aa830452
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849657"
---
# <span data-ttu-id="5edf4-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5edf4-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="5edf4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5edf4-102">SYNOPSIS</span></span>
<span data-ttu-id="5edf4-103">Felügyeli az Azure-tárterületet az Azure Storage-fiókokban.</span><span class="sxs-lookup"><span data-stu-id="5edf4-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5edf4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5edf4-104">SYNTAX</span></span>

### <span data-ttu-id="5edf4-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5edf4-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5edf4-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="5edf4-106">ByAccountName</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5edf4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5edf4-107">DESCRIPTION</span></span>
<span data-ttu-id="5edf4-108">Ha a fiók neve meg van adva, és a fiók kulcsait a megadott pince kezeli, akkor a rendszer egy fontos Vault-felügyelt Azure-tároló fiókot kap.</span><span class="sxs-lookup"><span data-stu-id="5edf4-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="5edf4-109">Ha a fióknév nincs megadva, akkor az összes olyan fiók szerepel a listában, amelynek kulcsait a megadott boltozat kezeli.</span><span class="sxs-lookup"><span data-stu-id="5edf4-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="5edf4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5edf4-110">EXAMPLES</span></span>

### <span data-ttu-id="5edf4-111">1. példa: az összes fontos boltíves kezelt tárolási fiók listázása</span><span class="sxs-lookup"><span data-stu-id="5edf4-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="5edf4-112">Felsorolja azokat a fiókokat, amelyek kulcsait a Vault ' myvault ' kezeli.</span><span class="sxs-lookup"><span data-stu-id="5edf4-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="5edf4-113">2. példa: fontos boltozatos tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="5edf4-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="5edf4-114">A "mystorageaccount" kulcs boltozatos tárterület-fiókjának részleteit kapja meg, ha a kulcsokat az "myvault" kezeli.</span><span class="sxs-lookup"><span data-stu-id="5edf4-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="5edf4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5edf4-115">PARAMETERS</span></span>

### <span data-ttu-id="5edf4-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5edf4-116">-AccountName</span></span>
<span data-ttu-id="5edf4-117">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="5edf4-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="5edf4-118">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="5edf4-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edf4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edf4-119">-DefaultProfile</span></span>
<span data-ttu-id="5edf4-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5edf4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5edf4-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5edf4-121">-VaultName</span></span>
<span data-ttu-id="5edf4-122">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="5edf4-122">Vault name.</span></span>
<span data-ttu-id="5edf4-123">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="5edf4-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="5edf4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edf4-124">CommonParameters</span></span>
<span data-ttu-id="5edf4-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5edf4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edf4-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5edf4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edf4-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5edf4-127">INPUTS</span></span>

### <span data-ttu-id="5edf4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5edf4-128">System.String</span></span>

## <span data-ttu-id="5edf4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5edf4-129">OUTPUTS</span></span>

### <span data-ttu-id="5edf4-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ManagedStorageAccount.............</span><span class="sxs-lookup"><span data-stu-id="5edf4-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5edf4-131">Microsoft. Azure. Command. ManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="5edf4-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="5edf4-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5edf4-132">NOTES</span></span>

## <span data-ttu-id="5edf4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5edf4-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

