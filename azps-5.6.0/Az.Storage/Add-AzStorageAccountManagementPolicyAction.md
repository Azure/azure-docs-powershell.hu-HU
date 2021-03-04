---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 65bce04c3df14a6b9dc4397d47577d0642746c45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930706"
---
# <span data-ttu-id="f4780-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f4780-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="f4780-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4780-102">SYNOPSIS</span></span>
<span data-ttu-id="f4780-103">Hozzáad egy műveletet a beviteli ManagementPolicy Action Group objektumhoz, vagy létrehoz egy ManagementPolicy Action Group objektumot a művelettel.</span><span class="sxs-lookup"><span data-stu-id="f4780-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="f4780-104">Az objektum használható a New-AzStorageAccountManagementPolicyRule-ban.</span><span class="sxs-lookup"><span data-stu-id="f4780-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="f4780-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f4780-105">SYNTAX</span></span>

### <span data-ttu-id="f4780-106">BaseBlob (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4780-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4780-107">Pillanatkép</span><span class="sxs-lookup"><span data-stu-id="f4780-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4780-108">BlobVersion</span><span class="sxs-lookup"><span data-stu-id="f4780-108">BlobVersion</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BlobVersionAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4780-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f4780-109">DESCRIPTION</span></span>
<span data-ttu-id="f4780-110">Az **Add-AzStorageAccountManagementPolicyAction** parancsmag hozzáad egy műveletet a input ManagementPolicy Action Group objektumhoz, vagy létrehoz egy ManagementPolicy Action Group objektumot a művelettel.</span><span class="sxs-lookup"><span data-stu-id="f4780-110">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="f4780-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f4780-111">EXAMPLES</span></span>

### <span data-ttu-id="f4780-112">1. példa: Létrehoz egy ManagementPolicy Action Group objektumot 4 műveletből, majd hozzáadja egy felügyeleti házirendszabályhoz, és tárhelyfiókra van állítva.</span><span class="sxs-lookup"><span data-stu-id="f4780-112">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100
Version.TierToCool.DaysAfterCreationGreaterThan         : 
Version.TierToArchive.DaysAfterCreationGreaterThan      : 
Version.Delete.DaysAfterCreationGreaterThan             : 

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="f4780-113">Az első parancs létrehoz egy ManagementPolicy Action Group objektumot, az alábbi 3 parancs 3 műveletet ad az objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="f4780-113">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="f4780-114">Ezután vegye fel egy felügyeleti házirendszabályba, és állítsa be tárfiókként.</span><span class="sxs-lookup"><span data-stu-id="f4780-114">Then add it to a management policy rule and set to a Storage account.</span></span>

### <span data-ttu-id="f4780-115">2. példa: Létrehoz egy ManagementPolicy Action Group objektumot 6 művelettel a pillanatkép és a blob verzióján, majd hozzáadja egy felügyeleti házirendszabályhoz, és tárhelyfiókra van állítva</span><span class="sxs-lookup"><span data-stu-id="f4780-115">Example 2: Creates a ManagementPolicy Action Group object with 6 actions on snapshot and blob version, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction  -SnapshotAction Delete -daysAfterCreationGreaterThan 40
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToArchive -daysAfterCreationGreaterThan 50
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToCool -daysAfterCreationGreaterThan 60
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction Delete -daysAfterCreationGreaterThan 70
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToArchive -daysAfterCreationGreaterThan 80
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToCool -daysAfterCreationGreaterThan 90
PS C:\> $action

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 60
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 50
Snapshot.Delete.DaysAfterCreationGreaterThan            : 40
Version.TierToCool.DaysAfterCreationGreaterThan         : 90
Version.TierToArchive.DaysAfterCreationGreaterThan      : 80
Version.Delete.DaysAfterCreationGreaterThan             : 70

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="f4780-116">Az első parancs létrehoz egy ManagementPolicy Action Group objektumot, az alábbi 5 parancs 5 műveletet ad hozzá a pillanatfelvételhez és a blobverzióhoz az objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="f4780-116">The first command create a ManagementPolicy Action Group object, the following 5 commands add 5 actions on snapshot and blob version to the object.</span></span> <span data-ttu-id="f4780-117">Ezután vegye fel egy felügyeleti házirendszabályba, és állítsa be tárfiókként.</span><span class="sxs-lookup"><span data-stu-id="f4780-117">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="f4780-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4780-118">PARAMETERS</span></span>

### <span data-ttu-id="f4780-119">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="f4780-119">-BaseBlobAction</span></span>
<span data-ttu-id="f4780-120">A baseblob kezelési házirend-művelete.</span><span class="sxs-lookup"><span data-stu-id="f4780-120">The management policy action for baseblob.</span></span>

```yaml
Type: System.String
Parameter Sets: BaseBlob
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4780-121">-BlobVersionAction</span><span class="sxs-lookup"><span data-stu-id="f4780-121">-BlobVersionAction</span></span>
<span data-ttu-id="f4780-122">A blobverzió felügyeleti házirend-művelete.</span><span class="sxs-lookup"><span data-stu-id="f4780-122">The management policy action for blob version.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobVersion
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4780-123">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="f4780-123">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="f4780-124">Egész szám, amely a létrehozás utáni napok korát jelzi.</span><span class="sxs-lookup"><span data-stu-id="f4780-124">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot, BlobVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4780-125">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="f4780-125">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="f4780-126">Egész szám, amely az utolsó módosítás utáni napok korát jelzi.</span><span class="sxs-lookup"><span data-stu-id="f4780-126">Integer value indicating the age in days after last modification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BaseBlob
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4780-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4780-127">-DefaultProfile</span></span>
<span data-ttu-id="f4780-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4780-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4780-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4780-129">-InputObject</span></span>
<span data-ttu-id="f4780-130">Ha a ManagementPolicy Action objektumot adja meg, a művelet bemeneti műveletobjektumra lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="f4780-130">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="f4780-131">Ha nem ad meg adatokat, új műveletobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f4780-131">If not input, will create a new action object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4780-132">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="f4780-132">-SnapshotAction</span></span>
<span data-ttu-id="f4780-133">A pillanatfelvétel felügyeleti házirend-művelete.</span><span class="sxs-lookup"><span data-stu-id="f4780-133">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4780-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4780-134">CommonParameters</span></span>
<span data-ttu-id="f4780-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4780-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4780-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4780-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4780-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4780-137">INPUTS</span></span>

### <span data-ttu-id="f4780-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="f4780-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="f4780-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4780-139">OUTPUTS</span></span>

### <span data-ttu-id="f4780-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="f4780-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="f4780-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f4780-141">NOTES</span></span>

## <span data-ttu-id="f4780-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4780-142">RELATED LINKS</span></span>
