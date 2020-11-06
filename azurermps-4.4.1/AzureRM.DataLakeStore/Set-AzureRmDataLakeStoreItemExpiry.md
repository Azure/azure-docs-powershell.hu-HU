---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: f71c26e69f9f297a23d4e6902ca6aaac6b135c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505956"
---
# <span data-ttu-id="a2a75-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="a2a75-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="a2a75-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2a75-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a75-103">Egy Azure Data Lake Store-fiókban lévő fájl elévülési idejének beállítása vagy eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a2a75-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2a75-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2a75-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2a75-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2a75-105">DESCRIPTION</span></span>
<span data-ttu-id="a2a75-106">A **set-AzureRmDataLakeStoreItemExpiry** parancsmag az Azure Data Lake Store-fiókban lévő fájlok elévülési idejét állítja be vagy távolítja el.</span><span class="sxs-lookup"><span data-stu-id="a2a75-106">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="a2a75-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a2a75-107">EXAMPLES</span></span>

### <span data-ttu-id="a2a75-108">1. példa: a fájl lejárati időpontjának beállítása</span><span class="sxs-lookup"><span data-stu-id="a2a75-108">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="a2a75-109">A lejárati myfile.txt a fiók ContosoADL, hogy most két óra legyen.</span><span class="sxs-lookup"><span data-stu-id="a2a75-109">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="a2a75-110">Ennek hatására két óra elteltével a fájl lejár (törlésre van megjelölve).</span><span class="sxs-lookup"><span data-stu-id="a2a75-110">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="a2a75-111">2. példa: a fájl elévülésének megszüntetése</span><span class="sxs-lookup"><span data-stu-id="a2a75-111">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="a2a75-112">A "ContosoADL" fiókban a "myfile.txt"-ra korábban beállított összes elévülési idő eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a2a75-112">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="a2a75-113">Ez azt jelenti, hogy a fájl nem jár le automatikusan (törlésre van megjelölve), és manuálisan kell törölnie vagy beállítani, hogy ismét lejárjon.</span><span class="sxs-lookup"><span data-stu-id="a2a75-113">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

## <span data-ttu-id="a2a75-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2a75-114">PARAMETERS</span></span>

### <span data-ttu-id="a2a75-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="a2a75-115">-Account</span></span>
<span data-ttu-id="a2a75-116">Az adattó áruházbeli fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2a75-116">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a75-117">-Lejárat</span><span class="sxs-lookup"><span data-stu-id="a2a75-117">-Expiration</span></span>
<span data-ttu-id="a2a75-118">A megadott fájl abszolút lejárati ideje.</span><span class="sxs-lookup"><span data-stu-id="a2a75-118">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="a2a75-119">Ha nincs érték vagy nincs beállítva a MaxValue, a fájl soha nem fog járni.</span><span class="sxs-lookup"><span data-stu-id="a2a75-119">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a75-120">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="a2a75-120">-Path</span></span>
<span data-ttu-id="a2a75-121">Az adattó-tároló elérési útját adja meg annak a fájlnak, amelyre vonatkozóan a lejárat után be kell állítani vagy el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="a2a75-121">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a75-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2a75-122">-Confirm</span></span>
<span data-ttu-id="a2a75-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2a75-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2a75-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2a75-124">-WhatIf</span></span>
<span data-ttu-id="a2a75-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2a75-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2a75-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2a75-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2a75-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a75-127">-DefaultProfile</span></span>
<span data-ttu-id="a2a75-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2a75-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a75-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a75-129">CommonParameters</span></span>
<span data-ttu-id="a2a75-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2a75-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a75-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2a75-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a75-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2a75-132">INPUTS</span></span>

## <span data-ttu-id="a2a75-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2a75-133">OUTPUTS</span></span>

### <span data-ttu-id="a2a75-134">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a2a75-134">DataLakeStoreItem</span></span>
<span data-ttu-id="a2a75-135">A frissített fájl új lejárati időponttal.</span><span class="sxs-lookup"><span data-stu-id="a2a75-135">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="a2a75-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2a75-136">NOTES</span></span>
<span data-ttu-id="a2a75-137">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="a2a75-137">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="a2a75-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2a75-138">RELATED LINKS</span></span>

[<span data-ttu-id="a2a75-139">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a2a75-139">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

