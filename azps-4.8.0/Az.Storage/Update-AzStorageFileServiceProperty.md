---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180757"
---
# <span data-ttu-id="05b92-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="05b92-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="05b92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05b92-102">SYNOPSIS</span></span>
<span data-ttu-id="05b92-103">Módosítja az Azure Storage file szolgáltatás tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="05b92-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="05b92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05b92-104">SYNTAX</span></span>

### <span data-ttu-id="05b92-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="05b92-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b92-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="05b92-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b92-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="05b92-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05b92-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="05b92-108">DESCRIPTION</span></span>
<span data-ttu-id="05b92-109">Az **Update-AzStorageFileServiceProperty** parancsmag módosította az Azure Storage file Service tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="05b92-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="05b92-110">Példák</span><span class="sxs-lookup"><span data-stu-id="05b92-110">EXAMPLES</span></span>

### <span data-ttu-id="05b92-111">1. példa: fájlmegosztási softdelete engedélyezése</span><span class="sxs-lookup"><span data-stu-id="05b92-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="05b92-112">Ez a parancs lehetővé teszi a fájlmegosztás softdelete törlését az 5 adatmegőrzési napokkal</span><span class="sxs-lookup"><span data-stu-id="05b92-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="05b92-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05b92-113">PARAMETERS</span></span>

### <span data-ttu-id="05b92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b92-114">-DefaultProfile</span></span>
<span data-ttu-id="05b92-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05b92-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05b92-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="05b92-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="05b92-117">A tárolási fiók megosztási törlési házirendjének engedélyezéséhez állítsa $true, tiltsa le a megosztás törlése adatmegőrzési házirendet a $false értékre.</span><span class="sxs-lookup"><span data-stu-id="05b92-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

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

### <span data-ttu-id="05b92-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05b92-118">-ResourceGroupName</span></span>
<span data-ttu-id="05b92-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="05b92-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="05b92-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05b92-120">-ResourceId</span></span>
<span data-ttu-id="05b92-121">Adja meg a tárolási fiók erőforrás-azonosítóját vagy a fájlkezelő tulajdonságok erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="05b92-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="05b92-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="05b92-122">-ShareRetentionDays</span></span>
<span data-ttu-id="05b92-123">Megadja a megosztási DeleteRetentionPolicy retenciós napjainak számát.</span><span class="sxs-lookup"><span data-stu-id="05b92-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="05b92-124">Az értéket csak akkor állítsa be, ha engedélyezi a megosztás törlése adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="05b92-124">The value should only be set when enable share Delete Retention Policy.</span></span>

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

### <span data-ttu-id="05b92-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="05b92-125">-StorageAccount</span></span>
<span data-ttu-id="05b92-126">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="05b92-126">Storage account object</span></span>

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

### <span data-ttu-id="05b92-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="05b92-127">-StorageAccountName</span></span>
<span data-ttu-id="05b92-128">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="05b92-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="05b92-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="05b92-129">-Confirm</span></span>
<span data-ttu-id="05b92-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="05b92-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05b92-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05b92-131">-WhatIf</span></span>
<span data-ttu-id="05b92-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="05b92-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05b92-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05b92-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05b92-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b92-134">CommonParameters</span></span>
<span data-ttu-id="05b92-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05b92-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b92-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05b92-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b92-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05b92-137">INPUTS</span></span>

### <span data-ttu-id="05b92-138">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05b92-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="05b92-139">System. String</span><span class="sxs-lookup"><span data-stu-id="05b92-139">System.String</span></span>

## <span data-ttu-id="05b92-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05b92-140">OUTPUTS</span></span>

### <span data-ttu-id="05b92-141">Microsoft. Azure. Command. Management. Storage. models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="05b92-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="05b92-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05b92-142">NOTES</span></span>

## <span data-ttu-id="05b92-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05b92-143">RELATED LINKS</span></span>
