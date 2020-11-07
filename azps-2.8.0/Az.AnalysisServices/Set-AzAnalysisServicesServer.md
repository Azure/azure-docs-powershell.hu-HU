---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: 376dc1cf74f93016cd0ce8e50d298cd2d12d6317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668153"
---
# <span data-ttu-id="d905c-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d905c-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="d905c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d905c-102">SYNOPSIS</span></span>
<span data-ttu-id="d905c-103">Az Analysis Services-kiszolgáló egy példányának módosítása</span><span class="sxs-lookup"><span data-stu-id="d905c-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="d905c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d905c-104">SYNTAX</span></span>

### <span data-ttu-id="d905c-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d905c-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d905c-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="d905c-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d905c-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="d905c-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d905c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d905c-108">DESCRIPTION</span></span>
<span data-ttu-id="d905c-109">A Set-AzAnalysisServicesServer parancsmag az Analysis Services-kiszolgáló egy példányát módosítja</span><span class="sxs-lookup"><span data-stu-id="d905c-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="d905c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d905c-110">EXAMPLES</span></span>

### <span data-ttu-id="d905c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d905c-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="d905c-112">Módosítja a TestServer nevű kiszolgálót a resourcegroup testgroup, hogy a címkéket key1: érték1 és azonosító2: érték2 testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d905c-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="d905c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d905c-113">PARAMETERS</span></span>

### <span data-ttu-id="d905c-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="d905c-114">-Administrator</span></span>
<span data-ttu-id="d905c-115">A kiszolgálón rendszergazdaként beállítani kívánt felhasználók vagy csoportok vesszővel elválasztott listáját megadó karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="d905c-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="d905c-116">A felhasználóknak vagy csoportoknak megadni kell egy UPN-formátumot (például user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d905c-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905c-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="d905c-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="d905c-118">A blob-tároló URI-ja az Analysis Services-kiszolgáló biztonsági mentéséhez</span><span class="sxs-lookup"><span data-stu-id="d905c-118">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905c-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="d905c-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="d905c-120">Az Analysis Service Server alapértelmezett csatlakozási módja</span><span class="sxs-lookup"><span data-stu-id="d905c-120">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d905c-121">-DefaultProfile</span></span>
<span data-ttu-id="d905c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d905c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d905c-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="d905c-123">-DisableBackup</span></span>
<span data-ttu-id="d905c-124">A biztonsági másolat blob-tárolójának letiltása a kapcsolóval.</span><span class="sxs-lookup"><span data-stu-id="d905c-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="d905c-125">A biztonsági másolat blob-tárolójának ismételt engedélyezéséhez adja meg a biztonsági másolat blob-tároló URI-BackupBlobContainerUriét.</span><span class="sxs-lookup"><span data-stu-id="d905c-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBackup
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905c-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="d905c-126">-DisassociateGateway</span></span>
<span data-ttu-id="d905c-127">Az átjáró erőforrás társítása az Analysis Serverből</span><span class="sxs-lookup"><span data-stu-id="d905c-127">Disassociate Gateway resource from an Analysis server</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisassociateGateway
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905c-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="d905c-128">-FirewallConfig</span></span>
<span data-ttu-id="d905c-129">Az Analysis-kiszolgálók tűzfal-konfigurációja</span><span class="sxs-lookup"><span data-stu-id="d905c-129">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905c-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d905c-130">-GatewayResourceId</span></span>
<span data-ttu-id="d905c-131">Átjáró erőforrás-azonosító társítása az Analysis Serverhez</span><span class="sxs-lookup"><span data-stu-id="d905c-131">Gateway resource Id to associate to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905c-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d905c-132">-Name</span></span>
<span data-ttu-id="d905c-133">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="d905c-133">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905c-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d905c-134">-PassThru</span></span>
<span data-ttu-id="d905c-135">A törölt kiszolgálói adatok visszaadása, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="d905c-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="d905c-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="d905c-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="d905c-137">Csak az Analysis Service Server-kiszolgálók replikáinak írásvédett száma</span><span class="sxs-lookup"><span data-stu-id="d905c-137">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d905c-138">-ResourceGroupName</span></span>
<span data-ttu-id="d905c-139">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="d905c-139">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905c-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="d905c-140">-Sku</span></span>
<span data-ttu-id="d905c-141">A kiszolgáló SKU-nak a neve.</span><span class="sxs-lookup"><span data-stu-id="d905c-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="d905c-142">A támogatott értékek 0 ', ' 1 ', ' 2 ', ' 4 ', a standard réteghez "B1", "B2" az alapszinthez és a 'D 1 ' for Development Tier.</span><span class="sxs-lookup"><span data-stu-id="d905c-142">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905c-143">-Címke</span><span class="sxs-lookup"><span data-stu-id="d905c-143">-Tag</span></span>
<span data-ttu-id="d905c-144">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="d905c-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905c-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d905c-145">-Confirm</span></span>
<span data-ttu-id="d905c-146">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="d905c-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="d905c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d905c-147">-WhatIf</span></span>
<span data-ttu-id="d905c-148">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="d905c-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="d905c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d905c-149">CommonParameters</span></span>
<span data-ttu-id="d905c-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d905c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d905c-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d905c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d905c-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d905c-152">INPUTS</span></span>

### <span data-ttu-id="d905c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d905c-153">System.String</span></span>

### <span data-ttu-id="d905c-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d905c-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d905c-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d905c-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d905c-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d905c-156">System.Int32</span></span>

### <span data-ttu-id="d905c-157">Microsoft. Azure. Command. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="d905c-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="d905c-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d905c-158">OUTPUTS</span></span>

### <span data-ttu-id="d905c-159">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d905c-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="d905c-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d905c-160">NOTES</span></span>
<span data-ttu-id="d905c-161">Alias: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="d905c-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="d905c-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d905c-162">RELATED LINKS</span></span>

[<span data-ttu-id="d905c-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d905c-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="d905c-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d905c-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
