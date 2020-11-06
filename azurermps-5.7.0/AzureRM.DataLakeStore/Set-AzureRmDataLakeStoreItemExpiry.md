---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 6908bc4d474d0dbe9df045332f3820b5f7536dac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500623"
---
# <span data-ttu-id="cac1e-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="cac1e-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="cac1e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cac1e-102">SYNOPSIS</span></span>
<span data-ttu-id="cac1e-103">Egy Azure Data Lake Store-fiókban lévő fájl elévülési idejének beállítása vagy eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="cac1e-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cac1e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cac1e-104">SYNTAX</span></span>

### <span data-ttu-id="cac1e-105">SetAbsoluteNeverExpireExpiry (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cac1e-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cac1e-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="cac1e-106">SetRelativeExpiry</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-RelativeFileExpiryOption] <PathRelativeExpiryOptions>] [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cac1e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cac1e-107">DESCRIPTION</span></span>
<span data-ttu-id="cac1e-108">A **set-AzureRmDataLakeStoreItemExpiry** parancsmag az Azure Data Lake Store-fiókban lévő fájlok elévülési idejét állítja be vagy távolítja el.</span><span class="sxs-lookup"><span data-stu-id="cac1e-108">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="cac1e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cac1e-109">EXAMPLES</span></span>

### <span data-ttu-id="cac1e-110">1. példa: a fájl lejárati időpontjának beállítása</span><span class="sxs-lookup"><span data-stu-id="cac1e-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="cac1e-111">A lejárati myfile.txt a fiók ContosoADL, hogy most két óra legyen.</span><span class="sxs-lookup"><span data-stu-id="cac1e-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="cac1e-112">Ennek hatására két óra elteltével a fájl lejár (törlésre van megjelölve).</span><span class="sxs-lookup"><span data-stu-id="cac1e-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="cac1e-113">2. példa: a fájl elévülésének megszüntetése</span><span class="sxs-lookup"><span data-stu-id="cac1e-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="cac1e-114">A "ContosoADL" fiókban a "myfile.txt"-ra korábban beállított összes elévülési idő eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="cac1e-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="cac1e-115">Ez azt jelenti, hogy a fájl nem jár le automatikusan (törlésre van megjelölve), és manuálisan kell törölnie vagy beállítani, hogy ismét lejárjon.</span><span class="sxs-lookup"><span data-stu-id="cac1e-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>


### <span data-ttu-id="cac1e-116">3. példa: a fájl elévülési idejének beállítása</span><span class="sxs-lookup"><span data-stu-id="cac1e-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="cac1e-117">Az első parancs beállítja a fájl/myfile.txt 240-as másodpercek lejárati idejét a kiszolgálón az aktuális időhöz viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="cac1e-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>

<span data-ttu-id="cac1e-118">A második parancs a fájl/myfile.txt 240-as másodpercek lejárati idejét állítja be a kiszolgálón a létrehozási időhöz viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="cac1e-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="cac1e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cac1e-119">PARAMETERS</span></span>

### <span data-ttu-id="cac1e-120">-Fiók</span><span class="sxs-lookup"><span data-stu-id="cac1e-120">-Account</span></span>
<span data-ttu-id="cac1e-121">Az adattó áruházbeli fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cac1e-121">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cac1e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac1e-122">-DefaultProfile</span></span>
<span data-ttu-id="cac1e-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cac1e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cac1e-124">-Lejárat</span><span class="sxs-lookup"><span data-stu-id="cac1e-124">-Expiration</span></span>
<span data-ttu-id="cac1e-125">A megadott fájl abszolút lejárati ideje.</span><span class="sxs-lookup"><span data-stu-id="cac1e-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="cac1e-126">Ha nincs érték vagy nincs beállítva a MaxValue, a fájl soha nem fog járni.</span><span class="sxs-lookup"><span data-stu-id="cac1e-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: Set expiry as Absolute or NeverExpire
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cac1e-127">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="cac1e-127">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="cac1e-128">A relatív lejárati lehetőségek.</span><span class="sxs-lookup"><span data-stu-id="cac1e-128">Relative expiry options.</span></span> <span data-ttu-id="cac1e-129">A RelativeToNow vagy a RelativeToCreationDate a jelenlegi beállítások</span><span class="sxs-lookup"><span data-stu-id="cac1e-129">RelativeToNow or RelativeToCreationDate are current options</span></span>
```yaml
Type: PathRelativeExpiryOptions
Parameter Sets: Set expiry as relative to creation or now
Aliases: 
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cac1e-130">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="cac1e-130">-Path</span></span>
<span data-ttu-id="cac1e-131">Az adattó-tároló elérési útját adja meg annak a fájlnak, amelyre vonatkozóan a lejárat után be kell állítani vagy el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="cac1e-131">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cac1e-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="cac1e-132">-RelativeTime</span></span>
<span data-ttu-id="cac1e-133">A relatív idő ezredmásodpercben a most vagy a létrehozási időponttal kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="cac1e-133">The relative time in milliseconds with respect to now or creation time</span></span>
```yaml
Type: Int64
Parameter Sets: Set expiry as relative to creation or now
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cac1e-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cac1e-134">-Confirm</span></span>
<span data-ttu-id="cac1e-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cac1e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cac1e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cac1e-136">-WhatIf</span></span>
<span data-ttu-id="cac1e-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cac1e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cac1e-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cac1e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cac1e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac1e-139">CommonParameters</span></span>
<span data-ttu-id="cac1e-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cac1e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac1e-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cac1e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac1e-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cac1e-142">INPUTS</span></span>

### <span data-ttu-id="cac1e-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="cac1e-143">None</span></span>
<span data-ttu-id="cac1e-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cac1e-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cac1e-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cac1e-145">OUTPUTS</span></span>

### <span data-ttu-id="cac1e-146">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cac1e-146">DataLakeStoreItem</span></span>
<span data-ttu-id="cac1e-147">A frissített fájl új lejárati időponttal.</span><span class="sxs-lookup"><span data-stu-id="cac1e-147">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="cac1e-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cac1e-148">NOTES</span></span>
<span data-ttu-id="cac1e-149">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="cac1e-149">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="cac1e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cac1e-150">RELATED LINKS</span></span>

[<span data-ttu-id="cac1e-151">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cac1e-151">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

