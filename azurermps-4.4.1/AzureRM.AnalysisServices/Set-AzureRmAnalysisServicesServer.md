---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 6bda63ad0c8e900a73c0ccd2afc506be7feae908
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492632"
---
# <span data-ttu-id="18b61-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="18b61-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="18b61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18b61-102">SYNOPSIS</span></span>
<span data-ttu-id="18b61-103">Az Analysis Services-kiszolgáló egy példányának módosítása</span><span class="sxs-lookup"><span data-stu-id="18b61-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18b61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18b61-104">SYNTAX</span></span>

### <span data-ttu-id="18b61-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18b61-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18b61-106">Biztonsági másolat letiltása</span><span class="sxs-lookup"><span data-stu-id="18b61-106">Disable Backup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18b61-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="18b61-107">DESCRIPTION</span></span>
<span data-ttu-id="18b61-108">A Set-AzureRmAnalysisServicesServer parancsmag az Analysis Services-kiszolgáló egy példányát módosítja</span><span class="sxs-lookup"><span data-stu-id="18b61-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="18b61-109">Példák</span><span class="sxs-lookup"><span data-stu-id="18b61-109">EXAMPLES</span></span>

### <span data-ttu-id="18b61-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="18b61-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="18b61-111">Módosítja a TestServer nevű kiszolgálót a resourcegroup testgroup, hogy a címkéket key1: érték1 és azonosító2: érték2 testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="18b61-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="18b61-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18b61-112">PARAMETERS</span></span>

### <span data-ttu-id="18b61-113">-Administrator</span><span class="sxs-lookup"><span data-stu-id="18b61-113">-Administrator</span></span>
<span data-ttu-id="18b61-114">A kiszolgálón rendszergazdaként beállítani kívánt felhasználók vagy csoportok vesszővel elválasztott listáját megadó karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="18b61-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="18b61-115">A felhasználóknak vagy csoportoknak megadni kell egy UPN-formátumot (például user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="18b61-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="18b61-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="18b61-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="18b61-117">A blob-tároló URI-ja az Analysis Services-kiszolgáló biztonsági mentéséhez</span><span class="sxs-lookup"><span data-stu-id="18b61-117">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="18b61-118">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="18b61-118">-DisableBackup</span></span>
<span data-ttu-id="18b61-119">A biztonsági másolat blob-tárolójának letiltása a kapcsolóval.</span><span class="sxs-lookup"><span data-stu-id="18b61-119">The switch to disable backup blob container.</span></span>
<span data-ttu-id="18b61-120">A biztonsági másolat blob-tárolójának ismételt engedélyezéséhez adja meg a biztonsági másolat blob-tároló URI-BackupBlobContainerUriét.</span><span class="sxs-lookup"><span data-stu-id="18b61-120">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Backup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b61-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18b61-121">-Name</span></span>
<span data-ttu-id="18b61-122">Az Analysis Services-kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="18b61-122">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="18b61-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18b61-123">-PassThru</span></span>
<span data-ttu-id="18b61-124">A törölt kiszolgálói adatok visszaadása, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="18b61-124">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="18b61-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b61-125">-ResourceGroupName</span></span>
<span data-ttu-id="18b61-126">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kiszolgáló tartozik</span><span class="sxs-lookup"><span data-stu-id="18b61-126">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="18b61-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="18b61-127">-Sku</span></span>
<span data-ttu-id="18b61-128">A kiszolgáló SKU-nak a neve.</span><span class="sxs-lookup"><span data-stu-id="18b61-128">The name of the Sku for the server.</span></span>
<span data-ttu-id="18b61-129">A támogatott értékek 0 ', ' 1 ', ' 2 ', ' 4 ', a standard réteghez "B1", "B2" az alapszinthez és a 'D 1 ' for Development Tier.</span><span class="sxs-lookup"><span data-stu-id="18b61-129">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="18b61-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="18b61-130">-Tag</span></span>
<span data-ttu-id="18b61-131">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="18b61-131">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="18b61-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="18b61-132">-Confirm</span></span>
<span data-ttu-id="18b61-133">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="18b61-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="18b61-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b61-134">-WhatIf</span></span>
<span data-ttu-id="18b61-135">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="18b61-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="18b61-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b61-136">-DefaultProfile</span></span>
<span data-ttu-id="18b61-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18b61-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18b61-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b61-138">CommonParameters</span></span>
<span data-ttu-id="18b61-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18b61-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b61-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b61-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b61-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18b61-141">INPUTS</span></span>

## <span data-ttu-id="18b61-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18b61-142">OUTPUTS</span></span>

### <span data-ttu-id="18b61-143">Microsoft. Azure. Management. Analysis. models. AnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="18b61-143">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="18b61-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18b61-144">NOTES</span></span>
<span data-ttu-id="18b61-145">Alias: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="18b61-145">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="18b61-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18b61-146">RELATED LINKS</span></span>

[<span data-ttu-id="18b61-147">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="18b61-147">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="18b61-148">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="18b61-148">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
