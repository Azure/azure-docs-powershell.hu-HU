---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 67c96d257be803e77555a7a93d8f9b1ebbbbf8c2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844325"
---
# <span data-ttu-id="7238a-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="7238a-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="7238a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7238a-102">SYNOPSIS</span></span>
<span data-ttu-id="7238a-103">Hozzáférés visszavonása a lemezhez</span><span class="sxs-lookup"><span data-stu-id="7238a-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="7238a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7238a-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7238a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7238a-105">DESCRIPTION</span></span>
<span data-ttu-id="7238a-106">A **Visszavonás-AzDiskAccess** parancsmag visszavonja a lemezhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="7238a-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="7238a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7238a-107">EXAMPLES</span></span>

### <span data-ttu-id="7238a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7238a-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="7238a-109">A "ResourceGroup01" nevű erőforráscsoport "Disk01" nevű lemezéhez való hozzáférés visszavonása</span><span class="sxs-lookup"><span data-stu-id="7238a-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="7238a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7238a-110">PARAMETERS</span></span>

### <span data-ttu-id="7238a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7238a-111">-AsJob</span></span>
<span data-ttu-id="7238a-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7238a-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7238a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7238a-113">-DefaultProfile</span></span>
<span data-ttu-id="7238a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7238a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7238a-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="7238a-115">-DiskName</span></span>
<span data-ttu-id="7238a-116">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7238a-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7238a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7238a-117">-ResourceGroupName</span></span>
<span data-ttu-id="7238a-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7238a-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7238a-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7238a-119">-Confirm</span></span>
<span data-ttu-id="7238a-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7238a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7238a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7238a-121">-WhatIf</span></span>
<span data-ttu-id="7238a-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7238a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7238a-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7238a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7238a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7238a-124">CommonParameters</span></span>
<span data-ttu-id="7238a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7238a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7238a-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7238a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7238a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7238a-127">INPUTS</span></span>

### <span data-ttu-id="7238a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7238a-128">System.String</span></span>

## <span data-ttu-id="7238a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7238a-129">OUTPUTS</span></span>

### <span data-ttu-id="7238a-130">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="7238a-130">System.Object</span></span>

## <span data-ttu-id="7238a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7238a-131">NOTES</span></span>

## <span data-ttu-id="7238a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7238a-132">RELATED LINKS</span></span>

