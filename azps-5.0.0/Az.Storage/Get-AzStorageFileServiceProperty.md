---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186348"
---
# <span data-ttu-id="aff7b-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="aff7b-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="aff7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aff7b-102">SYNOPSIS</span></span>
<span data-ttu-id="aff7b-103">Az Azure Storage file Services szolgáltatás tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="aff7b-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="aff7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aff7b-104">SYNTAX</span></span>

### <span data-ttu-id="aff7b-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aff7b-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aff7b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="aff7b-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aff7b-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="aff7b-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aff7b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aff7b-108">DESCRIPTION</span></span>
<span data-ttu-id="aff7b-109">A **Get-AzStorageFileServiceProperty** parancsmag az Azure Storage file Services szolgáltatás tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aff7b-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="aff7b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="aff7b-110">EXAMPLES</span></span>

### <span data-ttu-id="aff7b-111">Példa 1: az Azure Storage file Services tulajdonság beszerzése egy megadott tárterület-fiókból</span><span class="sxs-lookup"><span data-stu-id="aff7b-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="aff7b-112">Ez a parancs a megadott tárterület-fiók Fájlszolgáltatások tulajdonságát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aff7b-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="aff7b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aff7b-113">PARAMETERS</span></span>

### <span data-ttu-id="aff7b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff7b-114">-DefaultProfile</span></span>
<span data-ttu-id="aff7b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aff7b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aff7b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff7b-116">-ResourceGroupName</span></span>
<span data-ttu-id="aff7b-117">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="aff7b-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="aff7b-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aff7b-118">-ResourceId</span></span>
<span data-ttu-id="aff7b-119">Adja meg a tárolási fiók erőforrás-azonosítóját vagy a fájlkezelő tulajdonságok erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="aff7b-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aff7b-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="aff7b-120">-StorageAccount</span></span>
<span data-ttu-id="aff7b-121">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="aff7b-121">Storage account object</span></span>

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

### <span data-ttu-id="aff7b-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aff7b-122">-StorageAccountName</span></span>
<span data-ttu-id="aff7b-123">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="aff7b-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff7b-124">CommonParameters</span></span>
<span data-ttu-id="aff7b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aff7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff7b-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aff7b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff7b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aff7b-127">INPUTS</span></span>

### <span data-ttu-id="aff7b-128">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aff7b-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="aff7b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aff7b-129">System.String</span></span>

## <span data-ttu-id="aff7b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aff7b-130">OUTPUTS</span></span>

### <span data-ttu-id="aff7b-131">Microsoft. Azure. Command. Management. Storage. models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="aff7b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="aff7b-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aff7b-132">NOTES</span></span>

## <span data-ttu-id="aff7b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aff7b-133">RELATED LINKS</span></span>
