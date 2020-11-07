---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
ms.openlocfilehash: 6a1994979cc6521cee083b07f336a76a54dd7cb7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849653"
---
# <span data-ttu-id="424f4-101">Get-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="424f4-101">Get-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="424f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="424f4-102">SYNOPSIS</span></span>
<span data-ttu-id="424f4-103">Beolvassa a fontos Vault-tárolók biztonsági társításának definícióit.</span><span class="sxs-lookup"><span data-stu-id="424f4-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="424f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="424f4-104">SYNTAX</span></span>

### <span data-ttu-id="424f4-105">ByAccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="424f4-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="424f4-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="424f4-106">ByDefinitionName</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="424f4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="424f4-107">DESCRIPTION</span></span>
<span data-ttu-id="424f4-108">A felügyelt tárterületet tároló biztonsági társítási definíciót kapja, ha a definíció neve meg van adva.</span><span class="sxs-lookup"><span data-stu-id="424f4-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="424f4-109">Ha a definíció neve nincs megadva, akkor a rendszer a tárolóban a megadott kulcsos boltozat-fiókhoz társított összes SAS-definíciót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="424f4-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="424f4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="424f4-110">EXAMPLES</span></span>

### <span data-ttu-id="424f4-111">1. példa: az összes fontos Vault Managed Storage SAS definíciójának listázása</span><span class="sxs-lookup"><span data-stu-id="424f4-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="424f4-112">A "myvault" által kezelt "mystorageaccount" kulcs boltozattal kezelt tárterület-fiókkal társított összes biztonsági társítási definíció felsorolása</span><span class="sxs-lookup"><span data-stu-id="424f4-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="424f4-113">2. példa: fontos boltozatos tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="424f4-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="424f4-114">A "mysasDef" a "mystorageaccount" "myvault" által felügyelt "" című, a "" kulcs boltozat-definíciójának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="424f4-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="424f4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="424f4-115">PARAMETERS</span></span>

### <span data-ttu-id="424f4-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="424f4-116">-AccountName</span></span>
<span data-ttu-id="424f4-117">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="424f4-117">Vault name.</span></span>
<span data-ttu-id="424f4-118">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="424f4-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424f4-119">-DefaultProfile</span></span>
<span data-ttu-id="424f4-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="424f4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="424f4-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="424f4-121">-Name</span></span>
<span data-ttu-id="424f4-122">Storage sas-definíció neve.</span><span class="sxs-lookup"><span data-stu-id="424f4-122">Storage sas definition name.</span></span>
<span data-ttu-id="424f4-123">Parancsmag: a tároló biztonsági társításának FQDN-definícióját a boltozat neve, a jelenleg kijelölt környezet, a tárolási fiók neve és a sas-definíció neve alapján építi ki.</span><span class="sxs-lookup"><span data-stu-id="424f4-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424f4-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="424f4-124">-VaultName</span></span>
<span data-ttu-id="424f4-125">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="424f4-125">Vault name.</span></span>
<span data-ttu-id="424f4-126">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="424f4-126">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="424f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424f4-127">CommonParameters</span></span>
<span data-ttu-id="424f4-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="424f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424f4-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424f4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424f4-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="424f4-130">INPUTS</span></span>

### <span data-ttu-id="424f4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="424f4-131">System.String</span></span>

## <span data-ttu-id="424f4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="424f4-132">OUTPUTS</span></span>

### <span data-ttu-id="424f4-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ManagedStorageSasDefinitionListItem.............</span><span class="sxs-lookup"><span data-stu-id="424f4-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="424f4-134">Microsoft. Azure. Command. ManagedStorageSasDefinition. models.</span><span class="sxs-lookup"><span data-stu-id="424f4-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="424f4-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="424f4-135">NOTES</span></span>

## <span data-ttu-id="424f4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="424f4-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

