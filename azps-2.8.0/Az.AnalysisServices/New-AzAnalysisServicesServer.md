---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
ms.openlocfilehash: 1dc9546dd48285e1c2d6117578002d5aa523e5f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668162"
---
# <span data-ttu-id="cd61e-101">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="cd61e-101">New-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="cd61e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd61e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd61e-103">Új Analysis Services-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="cd61e-103">Creates a new Analysis Services server</span></span>

## <span data-ttu-id="cd61e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd61e-104">SYNTAX</span></span>

```
New-AzAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd61e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd61e-105">DESCRIPTION</span></span>
<span data-ttu-id="cd61e-106">Az New-AzAnalysisServicesServer parancsmag létrehoz egy új Analysis Services-kiszolgálót</span><span class="sxs-lookup"><span data-stu-id="cd61e-106">The New-AzAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="cd61e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd61e-107">EXAMPLES</span></span>

### <span data-ttu-id="cd61e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cd61e-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="cd61e-109">Létrehozza a TestServer nevű kiszolgálót az Azure region West-US és az erőforráscsoport testresourcegroup.</span><span class="sxs-lookup"><span data-stu-id="cd61e-109">Creates a server named testserver in the Azure region West-US and in resource group testresourcegroup.</span></span> <span data-ttu-id="cd61e-110">A kiszolgáló SKU-szintje S1 lesz.</span><span class="sxs-lookup"><span data-stu-id="cd61e-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="cd61e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd61e-111">PARAMETERS</span></span>

### <span data-ttu-id="cd61e-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="cd61e-112">-Administrator</span></span>
<span data-ttu-id="cd61e-113">A kiszolgálón rendszergazdaként beállítani kívánt felhasználók vagy csoportok vesszővel elválasztott listáját megadó karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="cd61e-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="cd61e-114">A felhasználóknak vagy csoportoknak megadni kell egy UPN-formátumot (például user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="cd61e-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd61e-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="cd61e-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="cd61e-116">A blob-tároló URI-ja az Analysis Services-kiszolgáló biztonsági mentéséhez</span><span class="sxs-lookup"><span data-stu-id="cd61e-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd61e-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="cd61e-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="cd61e-118">Az Analysis Service Server alapértelmezett csatlakozási módja</span><span class="sxs-lookup"><span data-stu-id="cd61e-118">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="cd61e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd61e-119">-DefaultProfile</span></span>
<span data-ttu-id="cd61e-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd61e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd61e-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="cd61e-121">-FirewallConfig</span></span>
<span data-ttu-id="cd61e-122">Az Analysis-kiszolgálók tűzfal-konfigurációja</span><span class="sxs-lookup"><span data-stu-id="cd61e-122">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="cd61e-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="cd61e-123">-GatewayResourceId</span></span>
<span data-ttu-id="cd61e-124">Átjáró erőforrás-azonosító társítása az Analysis Serverhez</span><span class="sxs-lookup"><span data-stu-id="cd61e-124">Gateway resource Id to associate to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd61e-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="cd61e-125">-Location</span></span>
<span data-ttu-id="cd61e-126">Az Azure-régió, ahol az Analysis Services-kiszolgáló van tárolva</span><span class="sxs-lookup"><span data-stu-id="cd61e-126">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd61e-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cd61e-127">-Name</span></span>
<span data-ttu-id="cd61e-128">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="cd61e-128">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd61e-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="cd61e-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="cd61e-130">Csak az Analysis Service Server-kiszolgálók replikáinak írásvédett száma</span><span class="sxs-lookup"><span data-stu-id="cd61e-130">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="cd61e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd61e-131">-ResourceGroupName</span></span>
<span data-ttu-id="cd61e-132">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="cd61e-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="cd61e-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="cd61e-133">-Sku</span></span>
<span data-ttu-id="cd61e-134">A kiszolgáló SKU-nak a neve.</span><span class="sxs-lookup"><span data-stu-id="cd61e-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="cd61e-135">A támogatott értékek 0 ', ' 1 ', ' 2 ', ' 4 ', a standard réteghez "B1", "B2" az alapszinthez és a 'D 1 ' for Development Tier.</span><span class="sxs-lookup"><span data-stu-id="cd61e-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd61e-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="cd61e-136">-Tag</span></span>
<span data-ttu-id="cd61e-137">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="cd61e-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd61e-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd61e-138">-Confirm</span></span>
<span data-ttu-id="cd61e-139">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="cd61e-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="cd61e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd61e-140">-WhatIf</span></span>
<span data-ttu-id="cd61e-141">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="cd61e-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="cd61e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd61e-142">CommonParameters</span></span>
<span data-ttu-id="cd61e-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd61e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd61e-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd61e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd61e-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd61e-145">INPUTS</span></span>

### <span data-ttu-id="cd61e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="cd61e-146">System.String</span></span>

### <span data-ttu-id="cd61e-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cd61e-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cd61e-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cd61e-148">System.Int32</span></span>

### <span data-ttu-id="cd61e-149">Microsoft. Azure. Command. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="cd61e-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="cd61e-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd61e-150">OUTPUTS</span></span>

### <span data-ttu-id="cd61e-151">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="cd61e-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="cd61e-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd61e-152">NOTES</span></span>
<span data-ttu-id="cd61e-153">Alias: New-AzAs</span><span class="sxs-lookup"><span data-stu-id="cd61e-153">Alias: New-AzAs</span></span>

## <span data-ttu-id="cd61e-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd61e-154">RELATED LINKS</span></span>

[<span data-ttu-id="cd61e-155">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="cd61e-155">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="cd61e-156">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="cd61e-156">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
