---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7c1b98f1d4408bddec94830a81bf06fa7c78baa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669768"
---
# <span data-ttu-id="22b9b-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="22b9b-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="22b9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="22b9b-103">Egy saját DNS-zónából törli a rekordot.</span><span class="sxs-lookup"><span data-stu-id="22b9b-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="22b9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22b9b-104">SYNTAX</span></span>

### <span data-ttu-id="22b9b-105">Mezők (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22b9b-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22b9b-106">Vegyes</span><span class="sxs-lookup"><span data-stu-id="22b9b-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b9b-107">Objektum</span><span class="sxs-lookup"><span data-stu-id="22b9b-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b9b-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="22b9b-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22b9b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="22b9b-109">DESCRIPTION</span></span>
<span data-ttu-id="22b9b-110">A Remove-AzPrivateDnsRecordSet parancsmag a megadott zónából törli a megadott rekordot.</span><span class="sxs-lookup"><span data-stu-id="22b9b-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="22b9b-111">A személyes zóna APEX-ben automatikusan létrehozott SOA-rekordok nem törölhetők.</span><span class="sxs-lookup"><span data-stu-id="22b9b-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="22b9b-112">A rekordhalmaz-objektum átadható erre a parancsmagra a pipeline operátorral, illetve paraméterként vagy ResourceId.</span><span class="sxs-lookup"><span data-stu-id="22b9b-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="22b9b-113">Ha a rekordokat név és típus szerint szeretné megadni a rekordhalmaz-objektum használata nélkül, a zónát PSPrivateDnsZone objektumként kell átadnia ehhez a parancsmaghoz a pipeline operátorral vagy paraméterként, illetve a ZoneName és a ResourceGroupName paramétert is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="22b9b-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="22b9b-114">A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.</span><span class="sxs-lookup"><span data-stu-id="22b9b-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="22b9b-115">Ha a rekordhalmazt RecordSet objektummal adja meg, akkor a program nem törli a rekordot, ha az Azure Private DNS-ben módosította a helyi RecordSet objektum beolvasását.</span><span class="sxs-lookup"><span data-stu-id="22b9b-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="22b9b-116">Ez védelmet nyújt az egyidejű módosítások számára.</span><span class="sxs-lookup"><span data-stu-id="22b9b-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="22b9b-117">Ezt úgy teheti meg, hogy a felülírási paramétert használja, amely a rekordokat az egyidejű módosításoktól függetlenül törli.</span><span class="sxs-lookup"><span data-stu-id="22b9b-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="22b9b-118">Példák</span><span class="sxs-lookup"><span data-stu-id="22b9b-118">EXAMPLES</span></span>

### <span data-ttu-id="22b9b-119">1. példa: a rekordtípus eltávolítása</span><span class="sxs-lookup"><span data-stu-id="22b9b-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="22b9b-120">Az első parancs a megadott rekordot kapja meg, majd a $RecordSet változóban tárolja. A második parancs eltávolítja a rekordot a $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="22b9b-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="22b9b-121">2. példa: a rekordtípus eltávolítása és az összes megerősítés letiltása</span><span class="sxs-lookup"><span data-stu-id="22b9b-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="22b9b-122">Az első parancs a megadott rekordot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="22b9b-122">The first command gets the specified record set.</span></span> <span data-ttu-id="22b9b-123">A második parancs törli a rekordot, még akkor is, ha időközben megváltozott.</span><span class="sxs-lookup"><span data-stu-id="22b9b-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="22b9b-124">A megerősítési utasításokat a rendszer letiltja.</span><span class="sxs-lookup"><span data-stu-id="22b9b-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="22b9b-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22b9b-125">PARAMETERS</span></span>

### <span data-ttu-id="22b9b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b9b-126">-DefaultProfile</span></span>
<span data-ttu-id="22b9b-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22b9b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b9b-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="22b9b-128">-Name</span></span>
<span data-ttu-id="22b9b-129">A rekordtípus rekordjainak neve (a zóna nevéhez és a végpontok nélküli ponthoz viszonyítva).</span><span class="sxs-lookup"><span data-stu-id="22b9b-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="22b9b-130">-Átír</span><span class="sxs-lookup"><span data-stu-id="22b9b-130">-Overwrite</span></span>
<span data-ttu-id="22b9b-131">Ne használja a ETag mezőt a rekordhalmaz paraméterben az optimista párhuzamossági ellenőrzésekhez.</span><span class="sxs-lookup"><span data-stu-id="22b9b-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="22b9b-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22b9b-132">-PassThru</span></span>
<span data-ttu-id="22b9b-133">A művelet eredményének (logikai) megadására szolgál a saját zóna további törlése a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="22b9b-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="22b9b-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="22b9b-134">-RecordSet</span></span>
<span data-ttu-id="22b9b-135">Az a rekord, amelybe be szeretné szúrni a rekordot.</span><span class="sxs-lookup"><span data-stu-id="22b9b-135">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="22b9b-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="22b9b-136">-RecordType</span></span>
<span data-ttu-id="22b9b-137">A saját DNS-rekordok típusa a rekordban.</span><span class="sxs-lookup"><span data-stu-id="22b9b-137">The type of Private DNS records in the record set.</span></span>

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

### <span data-ttu-id="22b9b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22b9b-138">-ResourceGroupName</span></span>
<span data-ttu-id="22b9b-139">Az az erőforráscsoport, amelyhez a zóna tartozik.</span><span class="sxs-lookup"><span data-stu-id="22b9b-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="22b9b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22b9b-140">-ResourceId</span></span>
<span data-ttu-id="22b9b-141">Privát DNS-RecprdSet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="22b9b-141">Private DNS RecprdSet ResourceID.</span></span>

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

### <span data-ttu-id="22b9b-142">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="22b9b-142">-Zone</span></span>
<span data-ttu-id="22b9b-143">Az a PrivateDnsZone objektum, amely a rekord létrehozásához használt zónát jelképezi.</span><span class="sxs-lookup"><span data-stu-id="22b9b-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="22b9b-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="22b9b-144">-ZoneName</span></span>
<span data-ttu-id="22b9b-145">Az a zóna, amelyben a rekord létezik (lezáró pont nélkül).</span><span class="sxs-lookup"><span data-stu-id="22b9b-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="22b9b-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="22b9b-146">-Confirm</span></span>
<span data-ttu-id="22b9b-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="22b9b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22b9b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22b9b-148">-WhatIf</span></span>
<span data-ttu-id="22b9b-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="22b9b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22b9b-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22b9b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22b9b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b9b-151">CommonParameters</span></span>
<span data-ttu-id="22b9b-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22b9b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b9b-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22b9b-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b9b-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22b9b-154">INPUTS</span></span>

### <span data-ttu-id="22b9b-155">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="22b9b-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="22b9b-156">Microsoft. Azure. Command. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="22b9b-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="22b9b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="22b9b-157">System.String</span></span>

## <span data-ttu-id="22b9b-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22b9b-158">OUTPUTS</span></span>

### <span data-ttu-id="22b9b-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22b9b-159">System.Boolean</span></span>

## <span data-ttu-id="22b9b-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22b9b-160">NOTES</span></span>

## <span data-ttu-id="22b9b-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22b9b-161">RELATED LINKS</span></span>
