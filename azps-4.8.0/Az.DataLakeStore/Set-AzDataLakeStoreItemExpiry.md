---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: ff769801c7a3496ab094e5c9877e0b53fb64fbfd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183651"
---
# <span data-ttu-id="0e6ba-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="0e6ba-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="0e6ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e6ba-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6ba-103">Egy Azure Data Lake Store-fiókban lévő fájl elévülési idejének beállítása vagy eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="0e6ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e6ba-104">SYNTAX</span></span>

### <span data-ttu-id="0e6ba-105">SetAbsoluteNeverExpireExpiry (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e6ba-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e6ba-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="0e6ba-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e6ba-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e6ba-107">DESCRIPTION</span></span>
<span data-ttu-id="0e6ba-108">A **set-AzDataLakeStoreItemExpiry** parancsmag az Azure Data Lake Store-fiókban lévő fájlok elévülési idejét állítja be vagy távolítja el.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="0e6ba-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0e6ba-109">EXAMPLES</span></span>

### <span data-ttu-id="0e6ba-110">1. példa: a fájl lejárati időpontjának beállítása</span><span class="sxs-lookup"><span data-stu-id="0e6ba-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="0e6ba-111">A lejárati myfile.txt a fiók ContosoADL, hogy most két óra legyen.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="0e6ba-112">Ennek hatására két óra elteltével a fájl lejár (törlésre van megjelölve).</span><span class="sxs-lookup"><span data-stu-id="0e6ba-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="0e6ba-113">2. példa: a fájl elévülésének megszüntetése</span><span class="sxs-lookup"><span data-stu-id="0e6ba-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="0e6ba-114">A "ContosoADL" fiókban a "myfile.txt"-ra korábban beállított összes elévülési idő eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="0e6ba-115">Ez azt jelenti, hogy a fájl nem jár le automatikusan (törlésre van megjelölve), és manuálisan kell törölnie vagy beállítani, hogy ismét lejárjon.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="0e6ba-116">3. példa: a fájl elévülési idejének beállítása</span><span class="sxs-lookup"><span data-stu-id="0e6ba-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="0e6ba-117">Az első parancs beállítja a fájl/myfile.txt 240-as másodpercek lejárati idejét a kiszolgálón az aktuális időhöz viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="0e6ba-118">A második parancs a fájl/myfile.txt 240-as másodpercek lejárati idejét állítja be a kiszolgálón a létrehozási időhöz viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="0e6ba-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e6ba-119">PARAMETERS</span></span>

### <span data-ttu-id="0e6ba-120">-Fiók</span><span class="sxs-lookup"><span data-stu-id="0e6ba-120">-Account</span></span>
<span data-ttu-id="0e6ba-121">Az adattó áruházbeli fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="0e6ba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6ba-122">-DefaultProfile</span></span>
<span data-ttu-id="0e6ba-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e6ba-124">-Lejárat</span><span class="sxs-lookup"><span data-stu-id="0e6ba-124">-Expiration</span></span>
<span data-ttu-id="0e6ba-125">A megadott fájl abszolút lejárati ideje.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="0e6ba-126">Ha nincs érték vagy nincs beállítva a MaxValue, a fájl soha nem fog járni.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e6ba-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="0e6ba-127">-Path</span></span>
<span data-ttu-id="0e6ba-128">Az adattó-tároló elérési útját adja meg annak a fájlnak, amelyre vonatkozóan a lejárat után be kell állítani vagy el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="0e6ba-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="0e6ba-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="0e6ba-130">A relatív lejárati lehetőségek.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-130">Relative expiry options.</span></span> <span data-ttu-id="0e6ba-131">A RelativeToNow vagy a RelativeToCreationDate a jelenlegi beállítások</span><span class="sxs-lookup"><span data-stu-id="0e6ba-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e6ba-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="0e6ba-132">-RelativeTime</span></span>
<span data-ttu-id="0e6ba-133">A relatív idő ezredmásodpercben a most vagy a létrehozási időponttal kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="0e6ba-133">The relative time in milliseconds with respect to now or creation time</span></span>

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e6ba-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0e6ba-134">-Confirm</span></span>
<span data-ttu-id="0e6ba-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e6ba-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e6ba-136">-WhatIf</span></span>
<span data-ttu-id="0e6ba-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e6ba-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e6ba-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e6ba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6ba-139">CommonParameters</span></span>
<span data-ttu-id="0e6ba-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e6ba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6ba-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e6ba-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6ba-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e6ba-142">INPUTS</span></span>

### <span data-ttu-id="0e6ba-143">System. String</span><span class="sxs-lookup"><span data-stu-id="0e6ba-143">System.String</span></span>

### <span data-ttu-id="0e6ba-144">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0e6ba-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="0e6ba-145">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0e6ba-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="0e6ba-146">Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreEnums + PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="0e6ba-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="0e6ba-147">System. Int64</span><span class="sxs-lookup"><span data-stu-id="0e6ba-147">System.Int64</span></span>

## <span data-ttu-id="0e6ba-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e6ba-148">OUTPUTS</span></span>

### <span data-ttu-id="0e6ba-149">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0e6ba-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="0e6ba-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e6ba-150">NOTES</span></span>
<span data-ttu-id="0e6ba-151">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="0e6ba-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="0e6ba-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e6ba-152">RELATED LINKS</span></span>

[<span data-ttu-id="0e6ba-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0e6ba-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

