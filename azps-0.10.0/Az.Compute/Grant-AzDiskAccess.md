---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: b7c5f713c7c245676804318b880df3f79a7ca60d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844529"
---
# <span data-ttu-id="1a2e7-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="1a2e7-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="1a2e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="1a2e7-103">Hozzáférést biztosít a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="1a2e7-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="1a2e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a2e7-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a2e7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a2e7-105">DESCRIPTION</span></span>
<span data-ttu-id="1a2e7-106">A **Grant-AzDiskAccess** parancsmag hozzáférést biztosít a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="1a2e7-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="1a2e7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1a2e7-107">EXAMPLES</span></span>

### <span data-ttu-id="1a2e7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1a2e7-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="1a2e7-109">Adjon "READ" hozzáférést a "ResourceGroup01" nevű erőforráscsoport "Disk01" nevű lemezéhez a 60-as másodpercben.</span><span class="sxs-lookup"><span data-stu-id="1a2e7-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="1a2e7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a2e7-110">PARAMETERS</span></span>

### <span data-ttu-id="1a2e7-111">-Access</span><span class="sxs-lookup"><span data-stu-id="1a2e7-111">-Access</span></span>
<span data-ttu-id="1a2e7-112">Hozzáférési szint megadása</span><span class="sxs-lookup"><span data-stu-id="1a2e7-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a2e7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a2e7-113">-AsJob</span></span>
<span data-ttu-id="1a2e7-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1a2e7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a2e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a2e7-115">-DefaultProfile</span></span>
<span data-ttu-id="1a2e7-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a2e7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a2e7-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="1a2e7-117">-DiskName</span></span>
<span data-ttu-id="1a2e7-118">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a2e7-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="1a2e7-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="1a2e7-119">-DurationInSecond</span></span>
<span data-ttu-id="1a2e7-120">A hozzáférési időtartamot másodpercben adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a2e7-120">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a2e7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a2e7-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a2e7-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a2e7-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1a2e7-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1a2e7-123">-Confirm</span></span>
<span data-ttu-id="1a2e7-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1a2e7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a2e7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a2e7-125">-WhatIf</span></span>
<span data-ttu-id="1a2e7-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1a2e7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a2e7-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1a2e7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a2e7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a2e7-128">CommonParameters</span></span>
<span data-ttu-id="1a2e7-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a2e7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a2e7-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a2e7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a2e7-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a2e7-131">INPUTS</span></span>

### <span data-ttu-id="1a2e7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1a2e7-132">System.String</span></span>

## <span data-ttu-id="1a2e7-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a2e7-133">OUTPUTS</span></span>

### <span data-ttu-id="1a2e7-134">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="1a2e7-134">System.Object</span></span>

## <span data-ttu-id="1a2e7-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a2e7-135">NOTES</span></span>

## <span data-ttu-id="1a2e7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a2e7-136">RELATED LINKS</span></span>

