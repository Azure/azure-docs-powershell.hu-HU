---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: ed876765e3b5eb9d306847958772d9205758f5d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143891"
---
# <span data-ttu-id="6e90f-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6e90f-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="6e90f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e90f-102">SYNOPSIS</span></span>
<span data-ttu-id="6e90f-103">Hozzáad egy műveletet a beviteli ManagementPolicy Action Group objektumhoz, vagy létrehoz egy ManagementPolicy Action Group objektumot a művelettel.</span><span class="sxs-lookup"><span data-stu-id="6e90f-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="6e90f-104">Az objektum használható a New-AzStorageAccountManagementPolicyRule-ban.</span><span class="sxs-lookup"><span data-stu-id="6e90f-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="6e90f-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e90f-105">SYNTAX</span></span>

### <span data-ttu-id="6e90f-106">BaseBlob (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e90f-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e90f-107">Pillanatkép</span><span class="sxs-lookup"><span data-stu-id="6e90f-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e90f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e90f-108">DESCRIPTION</span></span>
<span data-ttu-id="6e90f-109">Az **Add-AzStorageAccountManagementPolicyAction** parancsmag hozzáad egy műveletet a input ManagementPolicy Action Group objektumhoz, vagy létrehoz egy ManagementPolicy Action Group objektumot a művelettel.</span><span class="sxs-lookup"><span data-stu-id="6e90f-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="6e90f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e90f-110">EXAMPLES</span></span>

### <span data-ttu-id="6e90f-111">1. példa: Létrehoz egy ManagementPolicy Action Group objektumot 4 műveletből, majd hozzáadja egy felügyeleti házirendszabályhoz, és tárhelyfiókra van állítva</span><span class="sxs-lookup"><span data-stu-id="6e90f-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="6e90f-112">Az első parancs létrehoz egy ManagementPolicy Action Group objektumot, az alábbi 3 parancs 3 műveletet ad az objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="6e90f-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="6e90f-113">Ezután vegye fel egy felügyeleti házirendszabályba, és állítsa be tárfiókként.</span><span class="sxs-lookup"><span data-stu-id="6e90f-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="6e90f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e90f-114">PARAMETERS</span></span>

### <span data-ttu-id="6e90f-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="6e90f-115">-BaseBlobAction</span></span>
<span data-ttu-id="6e90f-116">A baseblob kezelési házirend-művelete.</span><span class="sxs-lookup"><span data-stu-id="6e90f-116">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="6e90f-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="6e90f-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="6e90f-118">Egész szám, amely a létrehozás utáni napok korát jelzi.</span><span class="sxs-lookup"><span data-stu-id="6e90f-118">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e90f-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="6e90f-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="6e90f-120">Egész szám, amely a legutóbbi módosítás utáni napok korát jelzi.</span><span class="sxs-lookup"><span data-stu-id="6e90f-120">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="6e90f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e90f-121">-DefaultProfile</span></span>
<span data-ttu-id="6e90f-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e90f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e90f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e90f-123">-InputObject</span></span>
<span data-ttu-id="6e90f-124">A ManagementPolicy Action objektum bevitele esetén a művelet a beviteli művelet objektumára lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="6e90f-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="6e90f-125">Ha nem ad meg adatokat, új műveletobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6e90f-125">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="6e90f-126">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="6e90f-126">-SnapshotAction</span></span>
<span data-ttu-id="6e90f-127">A pillanatfelvétel felügyeleti házirend-művelete.</span><span class="sxs-lookup"><span data-stu-id="6e90f-127">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e90f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e90f-128">CommonParameters</span></span>
<span data-ttu-id="6e90f-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e90f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e90f-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e90f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e90f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e90f-131">INPUTS</span></span>

### <span data-ttu-id="6e90f-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="6e90f-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="6e90f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e90f-133">OUTPUTS</span></span>

### <span data-ttu-id="6e90f-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="6e90f-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="6e90f-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e90f-135">NOTES</span></span>

## <span data-ttu-id="6e90f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e90f-136">RELATED LINKS</span></span>
