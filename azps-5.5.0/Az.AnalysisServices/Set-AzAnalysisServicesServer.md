---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: a3c3338db7fb749b3eb4d5e92c438deda0742a67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149618"
---
# <span data-ttu-id="2b738-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2b738-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="2b738-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b738-102">SYNOPSIS</span></span>
<span data-ttu-id="2b738-103">Módosítja az Analysis Services-kiszolgáló egy példányát</span><span class="sxs-lookup"><span data-stu-id="2b738-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="2b738-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b738-104">SYNTAX</span></span>

### <span data-ttu-id="2b738-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2b738-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b738-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="2b738-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b738-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="2b738-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b738-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b738-108">DESCRIPTION</span></span>
<span data-ttu-id="2b738-109">A Set-AzAnalysisServicesServer parancsmag módosítja az Analysis Services-kiszolgáló egy példányát</span><span class="sxs-lookup"><span data-stu-id="2b738-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="2b738-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b738-110">EXAMPLES</span></span>

### <span data-ttu-id="2b738-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2b738-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="2b738-112">Módosítja a testserver kiszolgálót az erőforráscsoport tesztcsoportban úgy, hogy a címkéket kulcs1:érték1 és key2:value2, illetve rendszergazdai kulcsként állítsa be testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="2b738-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="2b738-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b738-113">PARAMETERS</span></span>

### <span data-ttu-id="2b738-114">- Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="2b738-114">-Administrator</span></span>
<span data-ttu-id="2b738-115">A kiszolgálón rendszergazdaként beállítható felhasználók vagy csoportok vesszővel elválasztott listáját képviselő karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="2b738-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="2b738-116">A felhasználóknak vagy csoportoknak UPN formátumot kell megadnia, például user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="2b738-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="2b738-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="2b738-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="2b738-118">A blobtároló Uri az Analysis Services-kiszolgáló biztonsági mentéséhez</span><span class="sxs-lookup"><span data-stu-id="2b738-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="2b738-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="2b738-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="2b738-120">Az Analysis szolgáltatáskiszolgáló alapértelmezett csatlakozási módja</span><span class="sxs-lookup"><span data-stu-id="2b738-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="2b738-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b738-121">-DefaultProfile</span></span>
<span data-ttu-id="2b738-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b738-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b738-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="2b738-123">-DisableBackup</span></span>
<span data-ttu-id="2b738-124">A biztonságimásolat-blobtároló letiltására szolgáló kapcsoló.</span><span class="sxs-lookup"><span data-stu-id="2b738-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="2b738-125">A biztonságimásolat-blobtároló újra engedélyezéséhez adja meg a biztonságimásolat-blobtároló Uri-t -BackupBlobContainerUri fájlként.</span><span class="sxs-lookup"><span data-stu-id="2b738-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="2b738-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="2b738-126">-DisassociateGateway</span></span>
<span data-ttu-id="2b738-127">Átjáró típusú erőforrás társításának hozzárendelése analysis-kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="2b738-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="2b738-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="2b738-128">-FirewallConfig</span></span>
<span data-ttu-id="2b738-129">Analysis-kiszolgáló tűzfal-konfigurációja</span><span class="sxs-lookup"><span data-stu-id="2b738-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="2b738-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2b738-130">-GatewayResourceId</span></span>
<span data-ttu-id="2b738-131">Analysis-kiszolgálóhoz társítni szükséges átjáróerőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="2b738-131">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="2b738-132">-Name</span><span class="sxs-lookup"><span data-stu-id="2b738-132">-Name</span></span>
<span data-ttu-id="2b738-133">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="2b738-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="2b738-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b738-134">-PassThru</span></span>
<span data-ttu-id="2b738-135">A törölt kiszolgáló adatait adja vissza, ha a művelet sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="2b738-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="2b738-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="2b738-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="2b738-137">Az Analysis-szolgáltatáskiszolgálók egyetlen másolatszámának olvasása</span><span class="sxs-lookup"><span data-stu-id="2b738-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="2b738-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b738-138">-ResourceGroupName</span></span>
<span data-ttu-id="2b738-139">Annak az Azure-erőforráscsoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="2b738-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="2b738-140">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="2b738-140">-Sku</span></span>
<span data-ttu-id="2b738-141">A kiszolgáló termékváltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="2b738-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="2b738-142">A támogatott értékek a standard szint S0, S1, 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2'; "B1", "B2" az alapszinthez, a "D1" pedig a fejlesztési szinthez.</span><span class="sxs-lookup"><span data-stu-id="2b738-142">The supported values are 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="2b738-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b738-143">-Tag</span></span>
<span data-ttu-id="2b738-144">Kulcsérték-párok a kiszolgálón címkékként beállított kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="2b738-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="2b738-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b738-145">-Confirm</span></span>
<span data-ttu-id="2b738-146">Arra kéri a felhasználót, hogy erősítse meg a művelet elvégzését</span><span class="sxs-lookup"><span data-stu-id="2b738-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2b738-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b738-147">-WhatIf</span></span>
<span data-ttu-id="2b738-148">Az aktuális művelet által ténylegesen végrehajtott műveleteket ismerteti anélkül, hogy végrehajtaná őket.</span><span class="sxs-lookup"><span data-stu-id="2b738-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2b738-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b738-149">CommonParameters</span></span>
<span data-ttu-id="2b738-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b738-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b738-151">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b738-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b738-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b738-152">INPUTS</span></span>

### <span data-ttu-id="2b738-153">System.String</span><span class="sxs-lookup"><span data-stu-id="2b738-153">System.String</span></span>

### <span data-ttu-id="2b738-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2b738-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2b738-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2b738-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2b738-156">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2b738-156">System.Int32</span></span>

### <span data-ttu-id="2b738-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="2b738-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="2b738-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b738-158">OUTPUTS</span></span>

### <span data-ttu-id="2b738-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2b738-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="2b738-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b738-160">NOTES</span></span>
<span data-ttu-id="2b738-161">Alias: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="2b738-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="2b738-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b738-162">RELATED LINKS</span></span>

[<span data-ttu-id="2b738-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2b738-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="2b738-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2b738-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
