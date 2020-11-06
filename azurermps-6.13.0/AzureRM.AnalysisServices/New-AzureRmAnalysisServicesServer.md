---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: d8a795cc27a09fe7b23ac2156115d7a52212e3ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498575"
---
# <span data-ttu-id="58463-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="58463-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="58463-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="58463-102">SYNOPSIS</span></span>
<span data-ttu-id="58463-103">Új Analysis Services-kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="58463-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58463-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="58463-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58463-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="58463-105">DESCRIPTION</span></span>
<span data-ttu-id="58463-106">Az New-AzureRmAnalysisServicesServer parancsmag létrehoz egy új Analysis Services-kiszolgálót</span><span class="sxs-lookup"><span data-stu-id="58463-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="58463-107">Példák</span><span class="sxs-lookup"><span data-stu-id="58463-107">EXAMPLES</span></span>

### <span data-ttu-id="58463-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="58463-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="58463-109">Létrehozza a TestServer nevű kiszolgálót az Azure region West-US és az erőforráscsoport testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="58463-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="58463-110">A kiszolgáló SKU-szintje S1 lesz.</span><span class="sxs-lookup"><span data-stu-id="58463-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="58463-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="58463-111">PARAMETERS</span></span>

### <span data-ttu-id="58463-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="58463-112">-Administrator</span></span>
<span data-ttu-id="58463-113">A kiszolgálón rendszergazdaként beállítani kívánt felhasználók vagy csoportok vesszővel elválasztott listáját megadó karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="58463-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="58463-114">A felhasználóknak vagy csoportoknak megadni kell egy UPN-formátumot (például user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="58463-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="58463-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="58463-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="58463-116">A blob-tároló URI-ja az Analysis Services-kiszolgáló biztonsági mentéséhez</span><span class="sxs-lookup"><span data-stu-id="58463-116">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="58463-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="58463-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="58463-118">Az Analysis Service Server alapértelmezett csatlakozási módja</span><span class="sxs-lookup"><span data-stu-id="58463-118">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="58463-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58463-119">-DefaultProfile</span></span>
<span data-ttu-id="58463-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58463-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58463-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="58463-121">-FirewallConfig</span></span>
<span data-ttu-id="58463-122">Az Analysis-kiszolgálók tűzfal-konfigurációja</span><span class="sxs-lookup"><span data-stu-id="58463-122">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="58463-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="58463-123">-GatewayResourceId</span></span>
<span data-ttu-id="58463-124">Átjáró erőforrás-azonosítója a assocaite az Analysis Serverhez</span><span class="sxs-lookup"><span data-stu-id="58463-124">Gateway resource Id for assocaite to an Analysis server</span></span>

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

### <span data-ttu-id="58463-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="58463-125">-Location</span></span>
<span data-ttu-id="58463-126">Az Azure-régió, ahol az Analysis Services-kiszolgáló van tárolva</span><span class="sxs-lookup"><span data-stu-id="58463-126">The Azure region where the Analysis Services server is hosted</span></span>

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

### <span data-ttu-id="58463-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="58463-127">-Name</span></span>
<span data-ttu-id="58463-128">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="58463-128">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="58463-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="58463-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="58463-130">Csak az Analysis Service Server-kiszolgálók replikáinak írásvédett száma</span><span class="sxs-lookup"><span data-stu-id="58463-130">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="58463-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58463-131">-ResourceGroupName</span></span>
<span data-ttu-id="58463-132">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="58463-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="58463-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="58463-133">-Sku</span></span>
<span data-ttu-id="58463-134">A kiszolgáló SKU-nak a neve.</span><span class="sxs-lookup"><span data-stu-id="58463-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="58463-135">A támogatott értékek 0 ', ' 1 ', ' 2 ', ' 4 ', a standard réteghez "B1", "B2" az alapszinthez és a 'D 1 ' for Development Tier.</span><span class="sxs-lookup"><span data-stu-id="58463-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="58463-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="58463-136">-Tag</span></span>
<span data-ttu-id="58463-137">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="58463-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="58463-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="58463-138">-Confirm</span></span>
<span data-ttu-id="58463-139">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="58463-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="58463-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58463-140">-WhatIf</span></span>
<span data-ttu-id="58463-141">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="58463-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="58463-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58463-142">CommonParameters</span></span>
<span data-ttu-id="58463-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="58463-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58463-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58463-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58463-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="58463-145">INPUTS</span></span>

### <span data-ttu-id="58463-146">System. String</span><span class="sxs-lookup"><span data-stu-id="58463-146">System.String</span></span>

### <span data-ttu-id="58463-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="58463-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="58463-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="58463-148">System.Int32</span></span>

### <span data-ttu-id="58463-149">Microsoft. Azure. Command. AnalysisServices. models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="58463-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="58463-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58463-150">OUTPUTS</span></span>

### <span data-ttu-id="58463-151">Microsoft. Azure. Command. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="58463-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="58463-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="58463-152">NOTES</span></span>
<span data-ttu-id="58463-153">Alias: New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="58463-153">Alias: New-AzureAs</span></span>

## <span data-ttu-id="58463-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58463-154">RELATED LINKS</span></span>

[<span data-ttu-id="58463-155">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="58463-155">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="58463-156">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="58463-156">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
