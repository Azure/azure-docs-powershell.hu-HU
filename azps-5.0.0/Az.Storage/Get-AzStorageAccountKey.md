---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195472"
---
# <span data-ttu-id="26e20-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="26e20-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="26e20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26e20-102">SYNOPSIS</span></span>
<span data-ttu-id="26e20-103">Egy Azure-tárterülethez tartozó hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="26e20-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="26e20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26e20-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26e20-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="26e20-105">DESCRIPTION</span></span>
<span data-ttu-id="26e20-106">A **Get-AzStorageAccountKey** parancsmag a hozzáférési kulcsokat kapja meg egy Azure Storage-fiókban.</span><span class="sxs-lookup"><span data-stu-id="26e20-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="26e20-107">Példák</span><span class="sxs-lookup"><span data-stu-id="26e20-107">EXAMPLES</span></span>

### <span data-ttu-id="26e20-108">Példa 1: a tárolási fiók hozzáférési kulcsainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="26e20-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="26e20-109">Ez a parancs a megadott Azure Storage-fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="26e20-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="26e20-110">2. példa: speciális hozzáférési kulcs beszerzése tárterület-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="26e20-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="26e20-111">3. példa: a tárolási fiók elérési kulcsai (ha az Active Directory engedélyezve van) a Kerberos-kulcsok felvétele</span><span class="sxs-lookup"><span data-stu-id="26e20-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="26e20-112">Ez a parancs a megadott Azure Storage-fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="26e20-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="26e20-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26e20-113">PARAMETERS</span></span>

### <span data-ttu-id="26e20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e20-114">-DefaultProfile</span></span>
<span data-ttu-id="26e20-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26e20-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e20-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="26e20-116">-ListKerbKey</span></span>
<span data-ttu-id="26e20-117">Felsorolja a megadott tárterület-fiókhoz tartozó Kerberos-billentyűket (ha az Active Directory engedélyezve van).</span><span class="sxs-lookup"><span data-stu-id="26e20-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="26e20-118">Az Azure-fájlok identitás-hitelesítése az Azure Active Directory tartományi szolgáltatással (Azure AD DS) vagy az Active Directory tartományi szolgáltatással (AD DS) vagy az Active Directory tartományi szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="26e20-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="26e20-119">A rendszer a tartományi szolgáltatásban regisztrált identitás jelszavát használja, amely a tárolási fiókot jelenti.</span><span class="sxs-lookup"><span data-stu-id="26e20-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="26e20-120">A Kerberos-kulcs nem biztosít hozzáférési engedélyt semmilyen vezérlő vagy adatsíkon a tárolási fiókkal való olvasási vagy írási műveletek elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="26e20-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="26e20-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26e20-121">-Name</span></span>
<span data-ttu-id="26e20-122">Annak a tároló fióknak a nevét adja meg, amelyhez ez a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="26e20-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="26e20-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e20-123">-ResourceGroupName</span></span>
<span data-ttu-id="26e20-124">A tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26e20-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="26e20-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e20-125">CommonParameters</span></span>
<span data-ttu-id="26e20-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26e20-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e20-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e20-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e20-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26e20-128">INPUTS</span></span>

### <span data-ttu-id="26e20-129">System. String</span><span class="sxs-lookup"><span data-stu-id="26e20-129">System.String</span></span>

## <span data-ttu-id="26e20-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26e20-130">OUTPUTS</span></span>

### <span data-ttu-id="26e20-131">Microsoft. Azure. Management. Storage. models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="26e20-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="26e20-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26e20-132">NOTES</span></span>

## <span data-ttu-id="26e20-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26e20-133">RELATED LINKS</span></span>

[<span data-ttu-id="26e20-134">Új – AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="26e20-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


