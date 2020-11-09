---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: ff769801c7a3496ab094e5c9877e0b53fb64fbfd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297743"
---
# <span data-ttu-id="64e87-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="64e87-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="64e87-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64e87-102">SYNOPSIS</span></span>
<span data-ttu-id="64e87-103">Egy Azure Data Lake Store-fiókban lévő fájl elévülési idejének beállítása vagy eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="64e87-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="64e87-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64e87-104">SYNTAX</span></span>

### <span data-ttu-id="64e87-105">SetAbsoluteNeverExpireExpiry (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64e87-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64e87-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="64e87-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64e87-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="64e87-107">DESCRIPTION</span></span>
<span data-ttu-id="64e87-108">A **set-AzDataLakeStoreItemExpiry** parancsmag az Azure Data Lake Store-fiókban lévő fájlok elévülési idejét állítja be vagy távolítja el.</span><span class="sxs-lookup"><span data-stu-id="64e87-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="64e87-109">Példák</span><span class="sxs-lookup"><span data-stu-id="64e87-109">EXAMPLES</span></span>

### <span data-ttu-id="64e87-110">1. példa: a fájl lejárati időpontjának beállítása</span><span class="sxs-lookup"><span data-stu-id="64e87-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="64e87-111">A lejárati myfile.txt a fiók ContosoADL, hogy most két óra legyen.</span><span class="sxs-lookup"><span data-stu-id="64e87-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="64e87-112">Ennek hatására két óra elteltével a fájl lejár (törlésre van megjelölve).</span><span class="sxs-lookup"><span data-stu-id="64e87-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="64e87-113">2. példa: a fájl elévülésének megszüntetése</span><span class="sxs-lookup"><span data-stu-id="64e87-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="64e87-114">A "ContosoADL" fiókban a "myfile.txt"-ra korábban beállított összes elévülési idő eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="64e87-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="64e87-115">Ez azt jelenti, hogy a fájl nem jár le automatikusan (törlésre van megjelölve), és manuálisan kell törölnie vagy beállítani, hogy ismét lejárjon.</span><span class="sxs-lookup"><span data-stu-id="64e87-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="64e87-116">3. példa: a fájl elévülési idejének beállítása</span><span class="sxs-lookup"><span data-stu-id="64e87-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="64e87-117">Az első parancs beállítja a fájl/myfile.txt 240-as másodpercek lejárati idejét a kiszolgálón az aktuális időhöz viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="64e87-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="64e87-118">A második parancs a fájl/myfile.txt 240-as másodpercek lejárati idejét állítja be a kiszolgálón a létrehozási időhöz viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="64e87-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="64e87-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64e87-119">PARAMETERS</span></span>

### <span data-ttu-id="64e87-120">-Fiók</span><span class="sxs-lookup"><span data-stu-id="64e87-120">-Account</span></span>
<span data-ttu-id="64e87-121">Az adattó áruházbeli fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64e87-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="64e87-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64e87-122">-DefaultProfile</span></span>
<span data-ttu-id="64e87-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64e87-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64e87-124">-Lejárat</span><span class="sxs-lookup"><span data-stu-id="64e87-124">-Expiration</span></span>
<span data-ttu-id="64e87-125">A megadott fájl abszolút lejárati ideje.</span><span class="sxs-lookup"><span data-stu-id="64e87-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="64e87-126">Ha nincs érték vagy nincs beállítva a MaxValue, a fájl soha nem fog járni.</span><span class="sxs-lookup"><span data-stu-id="64e87-126">If no value or set to MaxValue, the file will never expire.</span></span>

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

### <span data-ttu-id="64e87-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="64e87-127">-Path</span></span>
<span data-ttu-id="64e87-128">Az adattó-tároló elérési útját adja meg annak a fájlnak, amelyre vonatkozóan a lejárat után be kell állítani vagy el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="64e87-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="64e87-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="64e87-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="64e87-130">A relatív lejárati lehetőségek.</span><span class="sxs-lookup"><span data-stu-id="64e87-130">Relative expiry options.</span></span> <span data-ttu-id="64e87-131">A RelativeToNow vagy a RelativeToCreationDate a jelenlegi beállítások</span><span class="sxs-lookup"><span data-stu-id="64e87-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

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

### <span data-ttu-id="64e87-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="64e87-132">-RelativeTime</span></span>
<span data-ttu-id="64e87-133">A relatív idő ezredmásodpercben a most vagy a létrehozási időponttal kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="64e87-133">The relative time in milliseconds with respect to now or creation time</span></span>

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

### <span data-ttu-id="64e87-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64e87-134">-Confirm</span></span>
<span data-ttu-id="64e87-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64e87-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64e87-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64e87-136">-WhatIf</span></span>
<span data-ttu-id="64e87-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64e87-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64e87-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64e87-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64e87-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64e87-139">CommonParameters</span></span>
<span data-ttu-id="64e87-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64e87-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64e87-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64e87-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64e87-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64e87-142">INPUTS</span></span>

### <span data-ttu-id="64e87-143">System. String</span><span class="sxs-lookup"><span data-stu-id="64e87-143">System.String</span></span>

### <span data-ttu-id="64e87-144">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="64e87-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="64e87-145">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="64e87-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="64e87-146">Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreEnums + PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="64e87-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="64e87-147">System. Int64</span><span class="sxs-lookup"><span data-stu-id="64e87-147">System.Int64</span></span>

## <span data-ttu-id="64e87-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64e87-148">OUTPUTS</span></span>

### <span data-ttu-id="64e87-149">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="64e87-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="64e87-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64e87-150">NOTES</span></span>
<span data-ttu-id="64e87-151">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="64e87-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="64e87-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64e87-152">RELATED LINKS</span></span>

[<span data-ttu-id="64e87-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="64e87-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

