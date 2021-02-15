---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: cdc2f8b1742625feb042865a9b75e2c495d7aac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145434"
---
# <span data-ttu-id="88b97-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="88b97-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="88b97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88b97-102">SYNOPSIS</span></span>
<span data-ttu-id="88b97-103">Tárfiók titkosítási hatókörének be- vagy listába való be szereznie vagy listába kell vennie a titkosítási hatókört.</span><span class="sxs-lookup"><span data-stu-id="88b97-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="88b97-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="88b97-104">SYNTAX</span></span>

### <span data-ttu-id="88b97-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88b97-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88b97-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="88b97-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88b97-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="88b97-107">DESCRIPTION</span></span>
<span data-ttu-id="88b97-108">A **Get-AzStorageEncryptionScope** parancsmag titkosítási hatókört kap vagy listázzon egy tárfiókból.</span><span class="sxs-lookup"><span data-stu-id="88b97-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="88b97-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="88b97-109">EXAMPLES</span></span>

### <span data-ttu-id="88b97-110">1. példa: Egyetlen titkosítási hatókör használata</span><span class="sxs-lookup"><span data-stu-id="88b97-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="88b97-111">Ez a parancs egyetlen titkosítási hatókört kap.</span><span class="sxs-lookup"><span data-stu-id="88b97-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="88b97-112">2. példa: Tárfiók összes titkosítási hatókörének felsorolása</span><span class="sxs-lookup"><span data-stu-id="88b97-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="88b97-113">Ez a parancs felsorolja a Tárfiók összes titkosítási hatókörét.</span><span class="sxs-lookup"><span data-stu-id="88b97-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="88b97-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88b97-114">PARAMETERS</span></span>

### <span data-ttu-id="88b97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b97-115">-DefaultProfile</span></span>
<span data-ttu-id="88b97-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88b97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b97-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="88b97-117">-EncryptionScopeName</span></span>
<span data-ttu-id="88b97-118">Azure Storage EncryptionScope-név</span><span class="sxs-lookup"><span data-stu-id="88b97-118">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b97-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b97-119">-ResourceGroupName</span></span>
<span data-ttu-id="88b97-120">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="88b97-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b97-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="88b97-121">-StorageAccount</span></span>
<span data-ttu-id="88b97-122">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="88b97-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88b97-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="88b97-123">-StorageAccountName</span></span>
<span data-ttu-id="88b97-124">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="88b97-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b97-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b97-125">CommonParameters</span></span>
<span data-ttu-id="88b97-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b97-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b97-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88b97-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b97-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88b97-128">INPUTS</span></span>

### <span data-ttu-id="88b97-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="88b97-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="88b97-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88b97-130">OUTPUTS</span></span>

### <span data-ttu-id="88b97-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="88b97-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="88b97-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="88b97-132">NOTES</span></span>

## <span data-ttu-id="88b97-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88b97-133">RELATED LINKS</span></span>
