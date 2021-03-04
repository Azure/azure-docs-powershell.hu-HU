---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: 7dd1fb194ebd14694b15914bdc9d633bb2973b20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941233"
---
# <span data-ttu-id="7f50d-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="7f50d-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="7f50d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f50d-102">SYNOPSIS</span></span>
<span data-ttu-id="7f50d-103">Beállítja vagy eltávolítja egy Azure Data Lake Store-fiókban tárolt fájl lejárati idejét.</span><span class="sxs-lookup"><span data-stu-id="7f50d-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="7f50d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f50d-104">SYNTAX</span></span>

### <span data-ttu-id="7f50d-105">SetAbsoluteNeverExpireExpiry (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f50d-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f50d-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="7f50d-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f50d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f50d-107">DESCRIPTION</span></span>
<span data-ttu-id="7f50d-108">A **Set-AzDataLakeStoreItemExpiry** parancsmag beállítja vagy eltávolítja egy Azure Data Lake Store-fiókban tárolt fájl lejárati idejét.</span><span class="sxs-lookup"><span data-stu-id="7f50d-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="7f50d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f50d-109">EXAMPLES</span></span>

### <span data-ttu-id="7f50d-110">1. példa: Fájl elévülési időének beállítása</span><span class="sxs-lookup"><span data-stu-id="7f50d-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="7f50d-111">A ContosoADL-myfile.txt elévülését két órára állítja be.</span><span class="sxs-lookup"><span data-stu-id="7f50d-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="7f50d-112">Ennek hatására a fájl két órán belül lejár (törlésre lesz megjelölve).</span><span class="sxs-lookup"><span data-stu-id="7f50d-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="7f50d-113">2. példa: Fájl elévülésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7f50d-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="7f50d-114">Eltávolítja a "ContosoADL" fiókban a fájlhoz korábban beállított myfile.txt elévülést.</span><span class="sxs-lookup"><span data-stu-id="7f50d-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="7f50d-115">Ez azt jelenti, hogy a fájl nem jár le automatikusan (törlésre lesz megjelölve), és manuálisan kell törölni, vagy újra elévülni.</span><span class="sxs-lookup"><span data-stu-id="7f50d-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="7f50d-116">3. példa: A fájl elévülési időének beállítása az adott időponthoz képest</span><span class="sxs-lookup"><span data-stu-id="7f50d-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="7f50d-117">Az első parancs 240 másodpercig állítja be a fájl /myfile.txt a kiszolgáló aktuális időéhez képest.</span><span class="sxs-lookup"><span data-stu-id="7f50d-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="7f50d-118">A második parancs 240 másodpercig állítja be a fájl /myfile.txt és a kiszolgálón való létrehozás idejét.</span><span class="sxs-lookup"><span data-stu-id="7f50d-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="7f50d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f50d-119">PARAMETERS</span></span>

### <span data-ttu-id="7f50d-120">-Account</span><span class="sxs-lookup"><span data-stu-id="7f50d-120">-Account</span></span>
<span data-ttu-id="7f50d-121">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f50d-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="7f50d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f50d-122">-DefaultProfile</span></span>
<span data-ttu-id="7f50d-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f50d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f50d-124">-Expiration</span><span class="sxs-lookup"><span data-stu-id="7f50d-124">-Expiration</span></span>
<span data-ttu-id="7f50d-125">A megadott fájl abszolút lejárati ideje.</span><span class="sxs-lookup"><span data-stu-id="7f50d-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="7f50d-126">Ha nincs érték vagy MaxValue érték, a fájl soha nem jár le.</span><span class="sxs-lookup"><span data-stu-id="7f50d-126">If no value or set to MaxValue, the file will never expire.</span></span>

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

### <span data-ttu-id="7f50d-127">-Path</span><span class="sxs-lookup"><span data-stu-id="7f50d-127">-Path</span></span>
<span data-ttu-id="7f50d-128">Annak a fájlelemnek a Data Lake Store-beli elérési útját adja meg, amelynek a lejáratát be szeretné állítani vagy el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="7f50d-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="7f50d-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="7f50d-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="7f50d-130">Relatív érvényesség-beállítások.</span><span class="sxs-lookup"><span data-stu-id="7f50d-130">Relative expiry options.</span></span> <span data-ttu-id="7f50d-131">A RelativeToNow vagy a RelativeToCreationDate aktuális beállítás</span><span class="sxs-lookup"><span data-stu-id="7f50d-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

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

### <span data-ttu-id="7f50d-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="7f50d-132">-RelativeTime</span></span>
<span data-ttu-id="7f50d-133">Az idő relatív idő ezredmásodpercben a következő időponthoz vagy a létrehozási időhez képest</span><span class="sxs-lookup"><span data-stu-id="7f50d-133">The relative time in milliseconds with respect to now or creation time</span></span>

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

### <span data-ttu-id="7f50d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f50d-134">-Confirm</span></span>
<span data-ttu-id="7f50d-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7f50d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f50d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f50d-136">-WhatIf</span></span>
<span data-ttu-id="7f50d-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7f50d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f50d-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f50d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f50d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f50d-139">CommonParameters</span></span>
<span data-ttu-id="7f50d-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f50d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f50d-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f50d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f50d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f50d-142">INPUTS</span></span>

### <span data-ttu-id="7f50d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7f50d-143">System.String</span></span>

### <span data-ttu-id="7f50d-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7f50d-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="7f50d-145">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7f50d-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="7f50d-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="7f50d-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="7f50d-147">System.Int64</span><span class="sxs-lookup"><span data-stu-id="7f50d-147">System.Int64</span></span>

## <span data-ttu-id="7f50d-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f50d-148">OUTPUTS</span></span>

### <span data-ttu-id="7f50d-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f50d-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="7f50d-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f50d-150">NOTES</span></span>
<span data-ttu-id="7f50d-151">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="7f50d-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="7f50d-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f50d-152">RELATED LINKS</span></span>

[<span data-ttu-id="7f50d-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f50d-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

