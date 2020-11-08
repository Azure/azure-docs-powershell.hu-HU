---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 6785eac6df5568f4b26e6de61ac0f4bfd8061259
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186347"
---
# <span data-ttu-id="df3fa-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="df3fa-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="df3fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df3fa-102">SYNOPSIS</span></span>
<span data-ttu-id="df3fa-103">A tárolási fiók objektum-replikációs házirendjének beolvasása vagy listázása.</span><span class="sxs-lookup"><span data-stu-id="df3fa-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="df3fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df3fa-104">SYNTAX</span></span>

### <span data-ttu-id="df3fa-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df3fa-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df3fa-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="df3fa-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df3fa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="df3fa-107">DESCRIPTION</span></span>
<span data-ttu-id="df3fa-108">A **Get-AzStorageObjectReplicationPolicy** parancsmag egy tárolási fiók objektum-replikációs házirendjét kapja vagy listázza.</span><span class="sxs-lookup"><span data-stu-id="df3fa-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="df3fa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="df3fa-109">EXAMPLES</span></span>

### <span data-ttu-id="df3fa-110">Példa 1: az objektum replikációs házirendjének beszerzése konkrét házirend-azonosítóval és a szabályok megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="df3fa-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
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

<span data-ttu-id="df3fa-111">Ez a parancs egy objektum replikációs házirendjét jeleníti meg konkrét házirend-azonosítóval, és megjeleníti annak szabályait.</span><span class="sxs-lookup"><span data-stu-id="df3fa-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="df3fa-112">2. példa: a List objektum replikációs házirendje egy tárterület-fiókból</span><span class="sxs-lookup"><span data-stu-id="df3fa-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="df3fa-113">Ez a parancs megjeleníti az objektum replikációs házirendjét egy tárterület-fiókból.</span><span class="sxs-lookup"><span data-stu-id="df3fa-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="df3fa-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df3fa-114">PARAMETERS</span></span>

### <span data-ttu-id="df3fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df3fa-115">-DefaultProfile</span></span>
<span data-ttu-id="df3fa-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df3fa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df3fa-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="df3fa-117">-PolicyId</span></span>
<span data-ttu-id="df3fa-118">Az objektum replikációs házirend-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="df3fa-118">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="df3fa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df3fa-119">-ResourceGroupName</span></span>
<span data-ttu-id="df3fa-120">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="df3fa-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="df3fa-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="df3fa-121">-StorageAccount</span></span>
<span data-ttu-id="df3fa-122">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="df3fa-122">Storage account object</span></span>

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

### <span data-ttu-id="df3fa-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="df3fa-123">-StorageAccountName</span></span>
<span data-ttu-id="df3fa-124">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="df3fa-124">Storage Account Name.</span></span>

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

### <span data-ttu-id="df3fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df3fa-125">CommonParameters</span></span>
<span data-ttu-id="df3fa-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df3fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df3fa-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df3fa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df3fa-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df3fa-128">INPUTS</span></span>

### <span data-ttu-id="df3fa-129">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="df3fa-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="df3fa-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df3fa-130">OUTPUTS</span></span>

### <span data-ttu-id="df3fa-131">Microsoft. Azure. Command. Management. Storage. models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="df3fa-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="df3fa-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df3fa-132">NOTES</span></span>

## <span data-ttu-id="df3fa-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df3fa-133">RELATED LINKS</span></span>
