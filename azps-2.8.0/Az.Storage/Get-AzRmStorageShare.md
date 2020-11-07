---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: f54196ef5b055a5e1968c682d21f861ee41c77ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839647"
---
# <span data-ttu-id="46d7b-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46d7b-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="46d7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="46d7b-103">Tárterület-megosztást kap vagy listáz.</span><span class="sxs-lookup"><span data-stu-id="46d7b-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="46d7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46d7b-104">SYNTAX</span></span>

### <span data-ttu-id="46d7b-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46d7b-105">AccountName (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46d7b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="46d7b-106">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46d7b-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="46d7b-107">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46d7b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="46d7b-108">DESCRIPTION</span></span>
<span data-ttu-id="46d7b-109">A **Get-AzRmStorageShare** parancsmag a tárterület-megosztásokat kapja vagy sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="46d7b-109">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="46d7b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="46d7b-110">EXAMPLES</span></span>

### <span data-ttu-id="46d7b-111">Példa 1: tárterület-megosztás beszerzése tárolási fiók nevével és megosztási névvel</span><span class="sxs-lookup"><span data-stu-id="46d7b-111">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="46d7b-112">Ez a parancs tárterület-megosztást kap a tárolási fióknév és a megosztási fiók nevével.</span><span class="sxs-lookup"><span data-stu-id="46d7b-112">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="46d7b-113">2. példa: tárterület-fiók tárterület-megosztásának listázása</span><span class="sxs-lookup"><span data-stu-id="46d7b-113">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
share2   myStorageAccount   myResourceGroup   "0x8D6FF862774FE57" 5120     2019-07-03 07:14:57Z
```

<span data-ttu-id="46d7b-114">Ebben a parancsban a tárolási fiók nevében tárolt tárterület-megosztások minden tárterülete látható.</span><span class="sxs-lookup"><span data-stu-id="46d7b-114">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="46d7b-115">3. példa: adattároló blob-tároló beszerzése tárolási fiók objektummal és tároló nevével</span><span class="sxs-lookup"><span data-stu-id="46d7b-115">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Get-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="46d7b-116">Ez a parancs egy tároló BLOB-tárolót kap a Storage Account objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="46d7b-116">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="46d7b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46d7b-117">PARAMETERS</span></span>

### <span data-ttu-id="46d7b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d7b-118">-DefaultProfile</span></span>
<span data-ttu-id="46d7b-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46d7b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46d7b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46d7b-120">-Name</span></span>
<span data-ttu-id="46d7b-121">Megosztás neve</span><span class="sxs-lookup"><span data-stu-id="46d7b-121">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d7b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d7b-122">-ResourceGroupName</span></span>
<span data-ttu-id="46d7b-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="46d7b-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46d7b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46d7b-124">-ResourceId</span></span>
<span data-ttu-id="46d7b-125">Adjon meg egy fájlmegosztási erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="46d7b-125">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46d7b-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="46d7b-126">-StorageAccount</span></span>
<span data-ttu-id="46d7b-127">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="46d7b-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d7b-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="46d7b-128">-StorageAccountName</span></span>
<span data-ttu-id="46d7b-129">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="46d7b-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46d7b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d7b-130">CommonParameters</span></span>
<span data-ttu-id="46d7b-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46d7b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d7b-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d7b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d7b-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46d7b-133">INPUTS</span></span>

### <span data-ttu-id="46d7b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="46d7b-134">System.String</span></span>

### <span data-ttu-id="46d7b-135">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46d7b-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="46d7b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46d7b-136">OUTPUTS</span></span>

### <span data-ttu-id="46d7b-137">Microsoft. Azure. Command. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="46d7b-137">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="46d7b-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46d7b-138">NOTES</span></span>

## <span data-ttu-id="46d7b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46d7b-139">RELATED LINKS</span></span>
