---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 15e11e9deedbc8a2e442d9b3f006511a98fd6394
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842145"
---
# <span data-ttu-id="b2036-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="b2036-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="b2036-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2036-102">SYNOPSIS</span></span>
<span data-ttu-id="b2036-103">Beolvassa a fontos Vault-tárolók biztonsági társításának definícióit.</span><span class="sxs-lookup"><span data-stu-id="b2036-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="b2036-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2036-104">SYNTAX</span></span>

### <span data-ttu-id="b2036-105">ByAccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2036-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2036-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b2036-106">ByDefinitionName</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2036-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2036-107">DESCRIPTION</span></span>
<span data-ttu-id="b2036-108">A felügyelt tárterületet tároló biztonsági társítási definíciót kapja, ha a definíció neve meg van adva.</span><span class="sxs-lookup"><span data-stu-id="b2036-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="b2036-109">Ha a definíció neve nincs megadva, akkor a rendszer a tárolóban a megadott kulcsos boltozat-fiókhoz társított összes SAS-definíciót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b2036-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="b2036-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b2036-110">EXAMPLES</span></span>

### <span data-ttu-id="b2036-111">1. példa: az összes fontos Vault Managed Storage SAS definíciójának listázása</span><span class="sxs-lookup"><span data-stu-id="b2036-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="b2036-112">A "myvault" által kezelt "mystorageaccount" kulcs boltozattal kezelt tárterület-fiókkal társított összes biztonsági társítási definíció felsorolása</span><span class="sxs-lookup"><span data-stu-id="b2036-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="b2036-113">2. példa: fontos boltozatos tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="b2036-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="b2036-114">A "mysasDef" a "mystorageaccount" "myvault" által felügyelt "" című, a "" kulcs boltozat-definíciójának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b2036-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="b2036-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2036-115">PARAMETERS</span></span>

### <span data-ttu-id="b2036-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b2036-116">-AccountName</span></span>
<span data-ttu-id="b2036-117">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="b2036-117">Vault name.</span></span>
<span data-ttu-id="b2036-118">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="b2036-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b2036-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2036-119">-DefaultProfile</span></span>
<span data-ttu-id="b2036-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b2036-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2036-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b2036-121">-Name</span></span>
<span data-ttu-id="b2036-122">Storage sas-definíció neve.</span><span class="sxs-lookup"><span data-stu-id="b2036-122">Storage sas definition name.</span></span>
<span data-ttu-id="b2036-123">Parancsmag: a tároló biztonsági társításának FQDN-definícióját a boltozat neve, a jelenleg kijelölt környezet, a tárolási fiók neve és a sas-definíció neve alapján építi ki.</span><span class="sxs-lookup"><span data-stu-id="b2036-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="b2036-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b2036-124">-VaultName</span></span>
<span data-ttu-id="b2036-125">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="b2036-125">Vault name.</span></span>
<span data-ttu-id="b2036-126">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="b2036-126">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b2036-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2036-127">CommonParameters</span></span>
<span data-ttu-id="b2036-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2036-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2036-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2036-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2036-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2036-130">INPUTS</span></span>

### <span data-ttu-id="b2036-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b2036-131">System.String</span></span>

## <span data-ttu-id="b2036-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2036-132">OUTPUTS</span></span>

### <span data-ttu-id="b2036-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ManagedStorageSasDefinitionListItem.............</span><span class="sxs-lookup"><span data-stu-id="b2036-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="b2036-134">Microsoft. Azure. Command. ManagedStorageSasDefinition. models.</span><span class="sxs-lookup"><span data-stu-id="b2036-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="b2036-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2036-135">NOTES</span></span>

## <span data-ttu-id="b2036-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2036-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

