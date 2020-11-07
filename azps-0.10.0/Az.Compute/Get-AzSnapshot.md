---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 25395cca287e7f711d5e124ab12919a0b5c01ce4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844658"
---
# <span data-ttu-id="19d6b-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="19d6b-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="19d6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="19d6b-103">A pillanatképek tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="19d6b-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="19d6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19d6b-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19d6b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19d6b-105">DESCRIPTION</span></span>
<span data-ttu-id="19d6b-106">A **Get-AzSnapshot** parancsmag a pillanatképek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19d6b-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="19d6b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="19d6b-107">EXAMPLES</span></span>

### <span data-ttu-id="19d6b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19d6b-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot
```

<span data-ttu-id="19d6b-109">Ez a parancs megkapja az előfizetés összes pillanatképének tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="19d6b-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="19d6b-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="19d6b-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="19d6b-111">Ez a parancs a "ResourceGroupName1" nevű erőforráscsoport összes pillanatképének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19d6b-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="19d6b-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="19d6b-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="19d6b-113">Ez a parancs a "ResourceGroupName1" nevű erőforráscsoport "SnapshotName1" nevű pillanatképének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="19d6b-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="19d6b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19d6b-114">PARAMETERS</span></span>

### <span data-ttu-id="19d6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d6b-115">-DefaultProfile</span></span>
<span data-ttu-id="19d6b-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19d6b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d6b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19d6b-117">-ResourceGroupName</span></span>
<span data-ttu-id="19d6b-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19d6b-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d6b-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="19d6b-119">-SnapshotName</span></span>
<span data-ttu-id="19d6b-120">A pillanatkép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19d6b-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d6b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d6b-121">CommonParameters</span></span>
<span data-ttu-id="19d6b-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19d6b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d6b-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19d6b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d6b-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19d6b-124">INPUTS</span></span>

### <span data-ttu-id="19d6b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="19d6b-125">System.String</span></span>

## <span data-ttu-id="19d6b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19d6b-126">OUTPUTS</span></span>

### <span data-ttu-id="19d6b-127">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="19d6b-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="19d6b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19d6b-128">NOTES</span></span>

## <span data-ttu-id="19d6b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19d6b-129">RELATED LINKS</span></span>

