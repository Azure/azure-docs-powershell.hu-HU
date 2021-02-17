---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164811"
---
# <span data-ttu-id="bdf8f-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bdf8f-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="bdf8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdf8f-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf8f-103">Lekérte egy Azure Storage-fiók hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="bdf8f-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="bdf8f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bdf8f-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdf8f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bdf8f-105">DESCRIPTION</span></span>
<span data-ttu-id="bdf8f-106">A **Get-AzStorageAccountKey** parancsmag az Azure Storage-fiók hozzáférési kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bdf8f-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="bdf8f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bdf8f-107">EXAMPLES</span></span>

### <span data-ttu-id="bdf8f-108">1. példa: Tárfiók hozzáférési kulcsának lekérte</span><span class="sxs-lookup"><span data-stu-id="bdf8f-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="bdf8f-109">Ez a parancs a megadott Azure Storage-fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bdf8f-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="bdf8f-110">2. példa: Tárfiók adott hozzáférési kulcsának lekérte</span><span class="sxs-lookup"><span data-stu-id="bdf8f-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="bdf8f-111">3. példa: A Tárfiók hozzáférési kulcsait sorolja fel, és tartalmazza a Kerberos-kulcsokat (ha engedélyezve van az Active Directory)</span><span class="sxs-lookup"><span data-stu-id="bdf8f-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="bdf8f-112">Ez a parancs a megadott Azure Storage-fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bdf8f-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="bdf8f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdf8f-113">PARAMETERS</span></span>

### <span data-ttu-id="bdf8f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf8f-114">-DefaultProfile</span></span>
<span data-ttu-id="bdf8f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdf8f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdf8f-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="bdf8f-116">-ListKerbKey</span></span>
<span data-ttu-id="bdf8f-117">A Kerberos-kulcsok listája (ha az Active Directory engedélyezve van) a megadott tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="bdf8f-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="bdf8f-118">A Kerberos-kulcs tárfiókonként jön létre Azure Files-identitásalapú hitelesítéshez azure Active Directory tartományi szolgáltatás (Azure AD DS) vagy Active Directory tartományi szolgáltatás (AD DS) segítségével.</span><span class="sxs-lookup"><span data-stu-id="bdf8f-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="bdf8f-119">A rendszer a tárfiókot képviselő tartományi szolgáltatásban regisztrált identitás jelszavaként használja.</span><span class="sxs-lookup"><span data-stu-id="bdf8f-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="bdf8f-120">A Kerberos-kulcs nem biztosít hozzáférési engedélyt arra, hogy vezérlő- vagy adat sík olvasási vagy írási műveleteket hajtson végre a tárfiókon.</span><span class="sxs-lookup"><span data-stu-id="bdf8f-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="bdf8f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bdf8f-121">-Name</span></span>
<span data-ttu-id="bdf8f-122">Annak a tárfióknak a nevét adja meg, amelyhez a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="bdf8f-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf8f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdf8f-123">-ResourceGroupName</span></span>
<span data-ttu-id="bdf8f-124">A Tárfiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdf8f-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="bdf8f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf8f-125">CommonParameters</span></span>
<span data-ttu-id="bdf8f-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf8f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf8f-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdf8f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf8f-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdf8f-128">INPUTS</span></span>

### <span data-ttu-id="bdf8f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bdf8f-129">System.String</span></span>

## <span data-ttu-id="bdf8f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdf8f-130">OUTPUTS</span></span>

### <span data-ttu-id="bdf8f-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bdf8f-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="bdf8f-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bdf8f-132">NOTES</span></span>

## <span data-ttu-id="bdf8f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdf8f-133">RELATED LINKS</span></span>

[<span data-ttu-id="bdf8f-134">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bdf8f-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


