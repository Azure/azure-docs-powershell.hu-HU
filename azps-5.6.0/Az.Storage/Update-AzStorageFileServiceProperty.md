---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: cb50a4fd4a50ee2f1d62a3abff338b7a4c77f4cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929225"
---
# <span data-ttu-id="02a4d-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="02a4d-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="02a4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="02a4d-103">Módosítja az Azure Storage File szolgáltatás szolgáltatás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="02a4d-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="02a4d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="02a4d-104">SYNTAX</span></span>

### <span data-ttu-id="02a4d-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02a4d-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a4d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="02a4d-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a4d-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="02a4d-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02a4d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="02a4d-108">DESCRIPTION</span></span>
<span data-ttu-id="02a4d-109">Az **Update-AzStorageFileServiceProperty** parancsmag módosítja az Azure Storage File szolgáltatás szolgáltatás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="02a4d-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="02a4d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="02a4d-110">EXAMPLES</span></span>

### <span data-ttu-id="02a4d-111">1. példa: A fájlmegosztás softdelete engedélyezése</span><span class="sxs-lookup"><span data-stu-id="02a4d-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName                            : mystorageaccount
ResourceGroupName                             : myresourcegroup
ShareDeleteRetentionPolicy.Enabled            : True
ShareDeleteRetentionPolicy.Days               : 5
```

<span data-ttu-id="02a4d-112">Ez a parancs lehetővé teszi a fájlmegosztás softdelete törlését 5 adatmegőrzési napokkal</span><span class="sxs-lookup"><span data-stu-id="02a4d-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="02a4d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02a4d-113">PARAMETERS</span></span>

### <span data-ttu-id="02a4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a4d-114">-DefaultProfile</span></span>
<span data-ttu-id="02a4d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02a4d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02a4d-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="02a4d-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="02a4d-117">Engedélyezze a tárfiók törlési adatmegőrzési házirend megosztását úgy, hogy $true, letiltja a megosztási adatmegőrzési házirendet úgy, hogy $false.</span><span class="sxs-lookup"><span data-stu-id="02a4d-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

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

### <span data-ttu-id="02a4d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a4d-118">-ResourceGroupName</span></span>
<span data-ttu-id="02a4d-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="02a4d-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="02a4d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02a4d-120">-ResourceId</span></span>
<span data-ttu-id="02a4d-121">Adja meg a tárfiók erőforrás-azonosítóját vagy egy fájlszolgáltatás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="02a4d-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="02a4d-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="02a4d-122">-ShareRetentionDays</span></span>
<span data-ttu-id="02a4d-123">Beállítja a megosztás DeleteRetentionPolicy adatmegőrzési napjainak számát.</span><span class="sxs-lookup"><span data-stu-id="02a4d-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="02a4d-124">Ezt az értéket csak akkor kell beállítani, ha engedélyezi a megosztási adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="02a4d-124">The value should only be set when enable share Delete Retention Policy.</span></span>

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

### <span data-ttu-id="02a4d-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="02a4d-125">-StorageAccount</span></span>
<span data-ttu-id="02a4d-126">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="02a4d-126">Storage account object</span></span>

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

### <span data-ttu-id="02a4d-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="02a4d-127">-StorageAccountName</span></span>
<span data-ttu-id="02a4d-128">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="02a4d-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="02a4d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02a4d-129">-Confirm</span></span>
<span data-ttu-id="02a4d-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="02a4d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a4d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a4d-131">-WhatIf</span></span>
<span data-ttu-id="02a4d-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="02a4d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a4d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02a4d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02a4d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a4d-134">CommonParameters</span></span>
<span data-ttu-id="02a4d-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a4d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a4d-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a4d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a4d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02a4d-137">INPUTS</span></span>

### <span data-ttu-id="02a4d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="02a4d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="02a4d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="02a4d-139">System.String</span></span>

## <span data-ttu-id="02a4d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02a4d-140">OUTPUTS</span></span>

### <span data-ttu-id="02a4d-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="02a4d-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="02a4d-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="02a4d-142">NOTES</span></span>

## <span data-ttu-id="02a4d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02a4d-143">RELATED LINKS</span></span>
