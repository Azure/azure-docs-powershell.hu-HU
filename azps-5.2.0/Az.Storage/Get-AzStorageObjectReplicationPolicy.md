---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 6785eac6df5568f4b26e6de61ac0f4bfd8061259
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349613"
---
# <span data-ttu-id="5304a-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="5304a-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="5304a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5304a-102">SYNOPSIS</span></span>
<span data-ttu-id="5304a-103">Egy tárfiók objektum-replikációs házirendját jeleníti meg vagy sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="5304a-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="5304a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5304a-104">SYNTAX</span></span>

### <span data-ttu-id="5304a-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5304a-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5304a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5304a-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5304a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5304a-107">DESCRIPTION</span></span>
<span data-ttu-id="5304a-108">A **Get-AzStorageObjectReplicationPolicy parancsmag** egy tárfiók objektum-replikációs házirendjeit kapja vagy sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="5304a-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="5304a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5304a-109">EXAMPLES</span></span>

### <span data-ttu-id="5304a-110">1. példa: Objektum-replikációs házirend lekérte adott házirend-azonosítót, és a szabály megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="5304a-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
```
PS C:\> $policy = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId 56bfa11c-81ef-4f8d-b307-5e5386e16fba

PS C:\> $policy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> $policy.Rules

RuleId                               SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------                               --------------- -------------------- ------------------- -----------------------
d3d39a01-8d92-40e5-849f-e56209ae5cf5 src1            dest1                {}                                         
2407de9a-3301-4656-858f-359d185565e0 src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="5304a-111">Ez a parancs egy objektum-replikációs házirendet kap adott házirend-azonosítóval, és annak szabályait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="5304a-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="5304a-112">2. példa: Objektumreplikációs házirend listása tárfiókból</span><span class="sxs-lookup"><span data-stu-id="5304a-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="5304a-113">Ez a parancs felsorolja a tárfiókból származó objektumreplikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="5304a-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="5304a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5304a-114">PARAMETERS</span></span>

### <span data-ttu-id="5304a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5304a-115">-DefaultProfile</span></span>
<span data-ttu-id="5304a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5304a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5304a-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="5304a-117">-PolicyId</span></span>
<span data-ttu-id="5304a-118">Objektum-replikációs házirend azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5304a-118">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5304a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5304a-119">-ResourceGroupName</span></span>
<span data-ttu-id="5304a-120">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5304a-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="5304a-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5304a-121">-StorageAccount</span></span>
<span data-ttu-id="5304a-122">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="5304a-122">Storage account object</span></span>

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

### <span data-ttu-id="5304a-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5304a-123">-StorageAccountName</span></span>
<span data-ttu-id="5304a-124">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="5304a-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5304a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5304a-125">CommonParameters</span></span>
<span data-ttu-id="5304a-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5304a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5304a-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5304a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5304a-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5304a-128">INPUTS</span></span>

### <span data-ttu-id="5304a-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5304a-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="5304a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5304a-130">OUTPUTS</span></span>

### <span data-ttu-id="5304a-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="5304a-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="5304a-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5304a-132">NOTES</span></span>

## <span data-ttu-id="5304a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5304a-133">RELATED LINKS</span></span>
