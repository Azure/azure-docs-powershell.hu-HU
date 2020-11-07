---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 73384827b5af2b3370eca1eee5a90066a89b8e55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668706"
---
# <span data-ttu-id="3d59a-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="3d59a-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="3d59a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d59a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d59a-103">Felvesz egy tevékenységet a bemeneti ManagementPolicy, vagy létrehoz egy ManagementPolicy-objektumot a művelettel.</span><span class="sxs-lookup"><span data-stu-id="3d59a-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="3d59a-104">Az objektum használható a New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="3d59a-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="3d59a-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d59a-105">SYNTAX</span></span>

### <span data-ttu-id="3d59a-106">BaseBlob (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3d59a-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d59a-107">Pillanatképként</span><span class="sxs-lookup"><span data-stu-id="3d59a-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d59a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d59a-108">DESCRIPTION</span></span>
<span data-ttu-id="3d59a-109">Az **Add-AzStorageAccountManagementPolicyAction** parancsmag felvesz egy tevékenységet a bemeneti ManagementPolicy, vagy létrehoz egy ManagementPolicy a művelettel.</span><span class="sxs-lookup"><span data-stu-id="3d59a-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="3d59a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3d59a-110">EXAMPLES</span></span>

### <span data-ttu-id="3d59a-111">1. példa: ManagementPolicy-műveleti csoport objektum létrehozása 4 művelettel, majd felvétele felügyeleti házirend-szabályba, és tárolási fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="3d59a-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
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

<span data-ttu-id="3d59a-112">Az első parancs ManagementPolicy-objektum létrehozásakor a következő 3 parancs hozzáadja a 3 műveletet az objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="3d59a-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="3d59a-113">Ezután adja hozzá egy felügyeleti házirend-szabályhoz, és állítsa be a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="3d59a-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="3d59a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d59a-114">PARAMETERS</span></span>

### <span data-ttu-id="3d59a-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="3d59a-115">-BaseBlobAction</span></span>
<span data-ttu-id="3d59a-116">A baseblob kezelési házirendje</span><span class="sxs-lookup"><span data-stu-id="3d59a-116">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="3d59a-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="3d59a-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="3d59a-118">Egész szám érték, amely a létrehozás után napokban a kor életkorát jelzi.</span><span class="sxs-lookup"><span data-stu-id="3d59a-118">Integer value indicating the age in days after creation.</span></span>

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

### <span data-ttu-id="3d59a-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="3d59a-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="3d59a-120">Egész érték, amely az utolsó módosítás után napokban a kor után látható.</span><span class="sxs-lookup"><span data-stu-id="3d59a-120">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="3d59a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d59a-121">-DefaultProfile</span></span>
<span data-ttu-id="3d59a-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d59a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d59a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d59a-123">-InputObject</span></span>
<span data-ttu-id="3d59a-124">Ha a ManagementPolicy művelet objektuma be van állítva, akkor a művelet a bemeneti művelet objektumra kerül.</span><span class="sxs-lookup"><span data-stu-id="3d59a-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="3d59a-125">Ha nincs bemenet, új műveleti objektum jön létre.</span><span class="sxs-lookup"><span data-stu-id="3d59a-125">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="3d59a-126">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="3d59a-126">-SnapshotAction</span></span>
<span data-ttu-id="3d59a-127">A pillanatképhez tartozó kezelési házirend-műveletek.</span><span class="sxs-lookup"><span data-stu-id="3d59a-127">The management policy action for snapshot.</span></span>

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

### <span data-ttu-id="3d59a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d59a-128">CommonParameters</span></span>
<span data-ttu-id="3d59a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d59a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d59a-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d59a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d59a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d59a-131">INPUTS</span></span>

### <span data-ttu-id="3d59a-132">Microsoft. Azure. Command. Management. Storage. models. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="3d59a-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="3d59a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d59a-133">OUTPUTS</span></span>

### <span data-ttu-id="3d59a-134">Microsoft. Azure. Command. Management. Storage. models. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="3d59a-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="3d59a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d59a-135">NOTES</span></span>

## <span data-ttu-id="3d59a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d59a-136">RELATED LINKS</span></span>
