---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/set-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 30f5e7237f497f3d9f4208548b56ede72583f067
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679226"
---
# <span data-ttu-id="baa19-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="baa19-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="baa19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="baa19-102">SYNOPSIS</span></span>
<span data-ttu-id="baa19-103">Az Analysis Services-kiszolgáló egy példányának módosítása</span><span class="sxs-lookup"><span data-stu-id="baa19-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baa19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="baa19-104">SYNTAX</span></span>

### <span data-ttu-id="baa19-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="baa19-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa19-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="baa19-106">DisableBackup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa19-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="baa19-107">DisassociateGateway</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baa19-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="baa19-108">DESCRIPTION</span></span>
<span data-ttu-id="baa19-109">A Set-AzureRmAnalysisServicesServer parancsmag az Analysis Services-kiszolgáló egy példányát módosítja</span><span class="sxs-lookup"><span data-stu-id="baa19-109">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="baa19-110">Példák</span><span class="sxs-lookup"><span data-stu-id="baa19-110">EXAMPLES</span></span>

### <span data-ttu-id="baa19-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="baa19-111">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="baa19-112">Módosítja a TestServer nevű kiszolgálót a resourcegroup testgroup, hogy a címkéket key1: érték1 és azonosító2: érték2 testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="baa19-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="baa19-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="baa19-113">PARAMETERS</span></span>

### <span data-ttu-id="baa19-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="baa19-114">-Administrator</span></span>
<span data-ttu-id="baa19-115">A kiszolgálón rendszergazdaként beállítani kívánt felhasználók vagy csoportok vesszővel elválasztott listáját megadó karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="baa19-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="baa19-116">A felhasználóknak vagy csoportoknak megadni kell egy UPN-formátumot (például user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="baa19-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="baa19-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="baa19-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="baa19-118">A blob-tároló URI-ja az Analysis Services-kiszolgáló biztonsági mentéséhez</span><span class="sxs-lookup"><span data-stu-id="baa19-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="baa19-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="baa19-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="baa19-120">Az Analysis Service Server alapértelmezett csatlakozási módja</span><span class="sxs-lookup"><span data-stu-id="baa19-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="baa19-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa19-121">-DefaultProfile</span></span>
<span data-ttu-id="baa19-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="baa19-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baa19-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="baa19-123">-DisableBackup</span></span>
<span data-ttu-id="baa19-124">A biztonsági másolat blob-tárolójának letiltása a kapcsolóval.</span><span class="sxs-lookup"><span data-stu-id="baa19-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="baa19-125">A biztonsági másolat blob-tárolójának ismételt engedélyezéséhez adja meg a biztonsági másolat blob-tároló URI-BackupBlobContainerUriét.</span><span class="sxs-lookup"><span data-stu-id="baa19-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="baa19-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="baa19-126">-DisassociateGateway</span></span>
<span data-ttu-id="baa19-127">Az átjáró erőforrás társítása az Analysis Serverből</span><span class="sxs-lookup"><span data-stu-id="baa19-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="baa19-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="baa19-128">-FirewallConfig</span></span>
<span data-ttu-id="baa19-129">Az Analysis-kiszolgálók tűzfal-konfigurációja</span><span class="sxs-lookup"><span data-stu-id="baa19-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="baa19-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="baa19-130">-GatewayResourceId</span></span>
<span data-ttu-id="baa19-131">Átjáró erőforrás-azonosítója a assocaite az Analysis Serverhez</span><span class="sxs-lookup"><span data-stu-id="baa19-131">Gateway resource Id for assocaite to an Analysis server</span></span>

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

### <span data-ttu-id="baa19-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="baa19-132">-Name</span></span>
<span data-ttu-id="baa19-133">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="baa19-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="baa19-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="baa19-134">-PassThru</span></span>
<span data-ttu-id="baa19-135">A törölt kiszolgálói adatok visszaadása, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="baa19-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="baa19-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="baa19-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="baa19-137">Csak az Analysis Service Server-kiszolgálók replikáinak írásvédett száma</span><span class="sxs-lookup"><span data-stu-id="baa19-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="baa19-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa19-138">-ResourceGroupName</span></span>
<span data-ttu-id="baa19-139">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="baa19-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="baa19-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="baa19-140">-Sku</span></span>
<span data-ttu-id="baa19-141">A kiszolgáló SKU-nak a neve.</span><span class="sxs-lookup"><span data-stu-id="baa19-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="baa19-142">A támogatott értékek 0 ', ' 1 ', ' 2 ', ' 4 ', a standard réteghez "B1", "B2" az alapszinthez és a 'D 1 ' for Development Tier.</span><span class="sxs-lookup"><span data-stu-id="baa19-142">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="baa19-143">-Címke</span><span class="sxs-lookup"><span data-stu-id="baa19-143">-Tag</span></span>
<span data-ttu-id="baa19-144">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="baa19-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="baa19-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="baa19-145">-Confirm</span></span>
<span data-ttu-id="baa19-146">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="baa19-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="baa19-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baa19-147">-WhatIf</span></span>
<span data-ttu-id="baa19-148">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="baa19-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="baa19-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa19-149">CommonParameters</span></span>
<span data-ttu-id="baa19-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="baa19-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa19-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baa19-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa19-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="baa19-152">INPUTS</span></span>

### <span data-ttu-id="baa19-153">System. String</span><span class="sxs-lookup"><span data-stu-id="baa19-153">System.String</span></span>

### <span data-ttu-id="baa19-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="baa19-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="baa19-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="baa19-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="baa19-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="baa19-156">System.Int32</span></span>

### <span data-ttu-id="baa19-157">Microsoft. Azure. Command. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="baa19-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="baa19-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="baa19-158">OUTPUTS</span></span>

### <span data-ttu-id="baa19-159">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="baa19-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="baa19-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="baa19-160">NOTES</span></span>
<span data-ttu-id="baa19-161">Alias: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="baa19-161">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="baa19-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="baa19-162">RELATED LINKS</span></span>

[<span data-ttu-id="baa19-163">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="baa19-163">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="baa19-164">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="baa19-164">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
