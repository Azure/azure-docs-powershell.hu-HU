---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302952"
---
# <span data-ttu-id="def95-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="def95-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="def95-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="def95-102">SYNOPSIS</span></span>
<span data-ttu-id="def95-103">Módosítja az Azure Storage file szolgáltatás tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="def95-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="def95-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="def95-104">SYNTAX</span></span>

### <span data-ttu-id="def95-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="def95-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="def95-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="def95-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="def95-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="def95-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="def95-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="def95-108">DESCRIPTION</span></span>
<span data-ttu-id="def95-109">Az **Update-AzStorageFileServiceProperty** parancsmag módosította az Azure Storage file Service tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="def95-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="def95-110">Példák</span><span class="sxs-lookup"><span data-stu-id="def95-110">EXAMPLES</span></span>

### <span data-ttu-id="def95-111">1. példa: fájlmegosztási softdelete engedélyezése</span><span class="sxs-lookup"><span data-stu-id="def95-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="def95-112">Ez a parancs lehetővé teszi a fájlmegosztás softdelete törlését az 5 adatmegőrzési napokkal</span><span class="sxs-lookup"><span data-stu-id="def95-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="def95-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="def95-113">PARAMETERS</span></span>

### <span data-ttu-id="def95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def95-114">-DefaultProfile</span></span>
<span data-ttu-id="def95-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="def95-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="def95-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="def95-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="def95-117">A tárolási fiók megosztási törlési házirendjének engedélyezéséhez állítsa $true, tiltsa le a megosztás törlése adatmegőrzési házirendet a $false értékre.</span><span class="sxs-lookup"><span data-stu-id="def95-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def95-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="def95-118">-ResourceGroupName</span></span>
<span data-ttu-id="def95-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="def95-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="def95-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="def95-120">-ResourceId</span></span>
<span data-ttu-id="def95-121">Adja meg a tárolási fiók erőforrás-azonosítóját vagy a fájlkezelő tulajdonságok erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="def95-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="def95-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="def95-122">-ShareRetentionDays</span></span>
<span data-ttu-id="def95-123">Megadja a megosztási DeleteRetentionPolicy retenciós napjainak számát.</span><span class="sxs-lookup"><span data-stu-id="def95-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="def95-124">Az értéket csak akkor állítsa be, ha engedélyezi a megosztás törlése adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="def95-124">The value should only be set when enable share Delete Retention Policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days, RetentionDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def95-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="def95-125">-StorageAccount</span></span>
<span data-ttu-id="def95-126">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="def95-126">Storage account object</span></span>

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

### <span data-ttu-id="def95-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="def95-127">-StorageAccountName</span></span>
<span data-ttu-id="def95-128">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="def95-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="def95-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="def95-129">-Confirm</span></span>
<span data-ttu-id="def95-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="def95-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def95-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="def95-131">-WhatIf</span></span>
<span data-ttu-id="def95-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="def95-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="def95-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="def95-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def95-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def95-134">CommonParameters</span></span>
<span data-ttu-id="def95-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="def95-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def95-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="def95-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def95-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="def95-137">INPUTS</span></span>

### <span data-ttu-id="def95-138">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="def95-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="def95-139">System. String</span><span class="sxs-lookup"><span data-stu-id="def95-139">System.String</span></span>

## <span data-ttu-id="def95-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="def95-140">OUTPUTS</span></span>

### <span data-ttu-id="def95-141">Microsoft. Azure. Command. Management. Storage. models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="def95-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="def95-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="def95-142">NOTES</span></span>

## <span data-ttu-id="def95-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="def95-143">RELATED LINKS</span></span>
