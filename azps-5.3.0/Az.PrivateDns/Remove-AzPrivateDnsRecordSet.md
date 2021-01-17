---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 865ab4ab3cca9d921fc8c40e9c6ae5cd03eaf00a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466681"
---
# <span data-ttu-id="c345c-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c345c-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="c345c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c345c-102">SYNOPSIS</span></span>
<span data-ttu-id="c345c-103">Töröl egy rekordkészletet egy privát DNS-zónából.</span><span class="sxs-lookup"><span data-stu-id="c345c-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="c345c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c345c-104">SYNTAX</span></span>

### <span data-ttu-id="c345c-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c345c-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c345c-106">Vegyes</span><span class="sxs-lookup"><span data-stu-id="c345c-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c345c-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="c345c-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c345c-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c345c-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c345c-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c345c-109">DESCRIPTION</span></span>
<span data-ttu-id="c345c-110">A Remove-AzPrivateDnsRecordSet parancsmag törli a megadott rekordkészletet a megadott zónából.</span><span class="sxs-lookup"><span data-stu-id="c345c-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="c345c-111">A privát zóna csúcsán automatikusan létrehozott SOA rekordok nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="c345c-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="c345c-112">A RecordSet-objektumot ehhez a parancsmaghoz a folyamat műveleti jelét használva, paraméterként vagy Erőforrásazonosítóként is át lehet adni.</span><span class="sxs-lookup"><span data-stu-id="c345c-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="c345c-113">Ha név szerint, majd RecordSet-objektum használata nélkül is megszeretné határozni a rekordkészletet, a zónát PSPrivateDnsZone-objektumként kell átadnia ehhez a parancsmaghoz a folyamat műveleti jelének vagy paramétereként, vagy megadhatja a ZoneName és az ResourceGroupName paramétert.</span><span class="sxs-lookup"><span data-stu-id="c345c-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="c345c-114">A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="c345c-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="c345c-115">Amikor rekordkészletet ad meg Egy RecordSet-objektummal, a rekordkészlet nem törlődik, ha módosult az Azure Private DNS-ben a helyi RecordSet objektum lekérése óta.</span><span class="sxs-lookup"><span data-stu-id="c345c-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="c345c-116">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="c345c-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="c345c-117">Ezt letilthatja a Felülírás paraméter használatával, amely törli a rekordkészletet az egyidejű módosításoktól függetlenül.</span><span class="sxs-lookup"><span data-stu-id="c345c-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="c345c-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c345c-118">EXAMPLES</span></span>

### <span data-ttu-id="c345c-119">1. példa: Rekordkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c345c-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="c345c-120">Az első parancs megkapja a megadott rekordkészletet, majd a $RecordSet tárolja. A második parancs eltávolítja a rekordkészletet a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="c345c-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="c345c-121">2. példa: Rekordkészlet eltávolítása és az összes megerősítés mellőzése</span><span class="sxs-lookup"><span data-stu-id="c345c-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="c345c-122">Az első parancs megkapja a megadott rekordkészletet.</span><span class="sxs-lookup"><span data-stu-id="c345c-122">The first command gets the specified record set.</span></span> <span data-ttu-id="c345c-123">A második parancs törli a rekordkészletet, még akkor is, ha időközben megváltozott.</span><span class="sxs-lookup"><span data-stu-id="c345c-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="c345c-124">A megerősítő kérések nincsenek letiltva.</span><span class="sxs-lookup"><span data-stu-id="c345c-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="c345c-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c345c-125">PARAMETERS</span></span>

### <span data-ttu-id="c345c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c345c-126">-DefaultProfile</span></span>
<span data-ttu-id="c345c-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c345c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c345c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c345c-128">-Name</span></span>
<span data-ttu-id="c345c-129">A rekordkészlet rekordjainak neve (a zóna nevéhez képest és befejezési pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="c345c-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c345c-130">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="c345c-130">-Overwrite</span></span>
<span data-ttu-id="c345c-131">Az optimista egyidejűség-ellenőrzéshez ne használja a RecordSet paraméter ETag mezőjét.</span><span class="sxs-lookup"><span data-stu-id="c345c-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c345c-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c345c-132">-PassThru</span></span>
<span data-ttu-id="c345c-133">A művelet eredményének (logikai) a folyamaton belül távolabbi privát zóna törlésére használható.</span><span class="sxs-lookup"><span data-stu-id="c345c-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c345c-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="c345c-134">-RecordSet</span></span>
<span data-ttu-id="c345c-135">Az a rekordkészlet, amelyben hozzá kell adni a rekordot.</span><span class="sxs-lookup"><span data-stu-id="c345c-135">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c345c-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="c345c-136">-RecordType</span></span>
<span data-ttu-id="c345c-137">A privát DNS-rekordok típusa a rekordkészletben.</span><span class="sxs-lookup"><span data-stu-id="c345c-137">The type of Private DNS records in the record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c345c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c345c-138">-ResourceGroupName</span></span>
<span data-ttu-id="c345c-139">Az az erőforráscsoport, amelyhez a zóna tartozik.</span><span class="sxs-lookup"><span data-stu-id="c345c-139">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c345c-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c345c-140">-ResourceId</span></span>
<span data-ttu-id="c345c-141">Private DNS RecordSet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="c345c-141">Private DNS RecordSet ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c345c-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="c345c-142">-Zone</span></span>
<span data-ttu-id="c345c-143">The PrivateDnsZone object representing the zone in which to create the record set.</span><span class="sxs-lookup"><span data-stu-id="c345c-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c345c-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="c345c-144">-ZoneName</span></span>
<span data-ttu-id="c345c-145">Az a zóna, amelyben a rekordkészlet létezik (befejezési pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="c345c-145">The zone in which the record set exists (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c345c-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c345c-146">-Confirm</span></span>
<span data-ttu-id="c345c-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c345c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c345c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c345c-148">-WhatIf</span></span>
<span data-ttu-id="c345c-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c345c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c345c-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c345c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c345c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c345c-151">CommonParameters</span></span>
<span data-ttu-id="c345c-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c345c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c345c-153">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c345c-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c345c-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c345c-154">INPUTS</span></span>

### <span data-ttu-id="c345c-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="c345c-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="c345c-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c345c-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="c345c-157">System.String</span><span class="sxs-lookup"><span data-stu-id="c345c-157">System.String</span></span>

## <span data-ttu-id="c345c-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c345c-158">OUTPUTS</span></span>

### <span data-ttu-id="c345c-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c345c-159">System.Boolean</span></span>

## <span data-ttu-id="c345c-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c345c-160">NOTES</span></span>

## <span data-ttu-id="c345c-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c345c-161">RELATED LINKS</span></span>
