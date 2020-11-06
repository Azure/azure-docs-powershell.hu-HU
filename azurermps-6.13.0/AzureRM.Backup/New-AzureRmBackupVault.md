---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: ad3619d2d0fcb9b60639a19b0c7d3fea45833857
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498471"
---
# <span data-ttu-id="b5fcb-101">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b5fcb-101">New-AzureRmBackupVault</span></span>

## <span data-ttu-id="b5fcb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fcb-103">Létrehoz egy biztonságimásolat-tárolót.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-103">Creates a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5fcb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5fcb-104">SYNTAX</span></span>

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5fcb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5fcb-105">DESCRIPTION</span></span>
<span data-ttu-id="b5fcb-106">A **New-AzureRmBackupVault** parancsmag egy Azure Backup boltozatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-106">The **New-AzureRmBackupVault** cmdlet creates an Azure Backup vault.</span></span>
<span data-ttu-id="b5fcb-107">Ez a parancsmag egy **AzureRmBackupVault** objektumot ad eredményül, amely a boltozat entitásra mutató hivatkozásként működik.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-107">This cmdlet returns an **AzureRmBackupVault** object that acts as a reference to the vault entity.</span></span>

## <span data-ttu-id="b5fcb-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b5fcb-108">EXAMPLES</span></span>

### <span data-ttu-id="b5fcb-109">1. példa: biztonságimásolat-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="b5fcb-109">Example 1: Create a backup vault</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="b5fcb-110">Ez a parancs létrehoz egy Vault03 nevű Azure Backup Vault-t.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-110">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="b5fcb-111">A boltozat a ResourceGroup01 nevű erőforrás-csoportban található a West US régióban.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-111">The vault is in the resource group named ResourceGroup01 in the West US region.</span></span>
<span data-ttu-id="b5fcb-112">A boltozat az alapértelmezett GeoRedundant-tárolási típust használja.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-112">The vault uses the default GeoRedundant storage type.</span></span>

### <span data-ttu-id="b5fcb-113">2. példa: helyileg redundáns tárterületet használó biztonságimásolat-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="b5fcb-113">Example 2: Create a backup vault that uses locally redundant storage</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

<span data-ttu-id="b5fcb-114">Ez a parancs létrehoz egy Vault03 nevű Azure Backup Vault-t.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-114">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="b5fcb-115">A boltozat a ResourceGroup02 nevű erőforrás-csoportban található a West US régióban.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-115">The vault is in the resource group named ResourceGroup02 in the West US region.</span></span>
<span data-ttu-id="b5fcb-116">A boltozat a LocallyRedundant-tároló típusát használja.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-116">The vault uses the LocallyRedundant storage type.</span></span>

## <span data-ttu-id="b5fcb-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5fcb-117">PARAMETERS</span></span>

### <span data-ttu-id="b5fcb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5fcb-118">-DefaultProfile</span></span>
<span data-ttu-id="b5fcb-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b5fcb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5fcb-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5fcb-120">-Name</span></span>
<span data-ttu-id="b5fcb-121">Az Azure Backup Vault nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-121">Specifies a name for the Azure Backup vault.</span></span>
<span data-ttu-id="b5fcb-122">A névnek egyedinek kell lennie egy erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-122">The name must be unique in a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fcb-123">-Region (régió)</span><span class="sxs-lookup"><span data-stu-id="b5fcb-123">-Region</span></span>
<span data-ttu-id="b5fcb-124">Itt adhatja meg azt az Azure-körzetet, amelyben a biztonságimásolat-tároló található.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-124">Specifies an Azure region in which the backup vault exists.</span></span>
<span data-ttu-id="b5fcb-125">A hibrid biztonságimásolat-forgatókönyvek esetében azt javasoljuk, hogy a helyi kiszolgálóhoz közeli területen hozzon létre egy boltozatot a késés csökkentéséhez.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-125">For hybrid backup scenarios, we recommend that you create a vault in a region close to the on-premise server to reduce latency.</span></span>
<span data-ttu-id="b5fcb-126">Az Azure Infrastructure biztonsági másolatának (IaaS) virtuális gépei esetén a boltozat a helyi virtuális gépek felderítési pontja lesz.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-126">For backup of Azure infrastructure as a service (IaaS) virtual machines, the vault becomes the point of discovery for local virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fcb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5fcb-127">-ResourceGroupName</span></span>
<span data-ttu-id="b5fcb-128">Annak a meglévő Azure erőforrás-csoportnak a nevét adja meg, amelyben ez a parancsmag létrehoz egy biztonságimásolat-tárolót.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-128">Specifies the name of an existing Azure resource group in which this cmdlet creates a Backup vault.</span></span>
<span data-ttu-id="b5fcb-129">Erőforráscsoport létrehozásához használja az New-AzureRMResourceGroup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-129">To create a resource group, use the New-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="b5fcb-130">Az erőforráscsoport és az Azure Backup Vault nem kell ugyanazon a területen lennie.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-130">The resource group and the Azure Backup vault do not have to be in the same region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fcb-131">-Tárterület</span><span class="sxs-lookup"><span data-stu-id="b5fcb-131">-Storage</span></span>
<span data-ttu-id="b5fcb-132">A biztonsági másolat adatainak tárolási típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-132">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="b5fcb-133">A paraméter elfogadható értékei a következők: LocallyRedundant és GeoRedundant.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-133">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>
<span data-ttu-id="b5fcb-134">Az alapértelmezett érték a GeoRedundant.</span><span class="sxs-lookup"><span data-stu-id="b5fcb-134">The default value is GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fcb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fcb-135">CommonParameters</span></span>
<span data-ttu-id="b5fcb-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5fcb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5fcb-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5fcb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fcb-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5fcb-138">INPUTS</span></span>

### <span data-ttu-id="b5fcb-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="b5fcb-139">None</span></span>

## <span data-ttu-id="b5fcb-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5fcb-140">OUTPUTS</span></span>

### <span data-ttu-id="b5fcb-141">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="b5fcb-141">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>

## <span data-ttu-id="b5fcb-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5fcb-142">NOTES</span></span>
* <span data-ttu-id="b5fcb-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="b5fcb-143">None</span></span>

## <span data-ttu-id="b5fcb-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5fcb-144">RELATED LINKS</span></span>

[<span data-ttu-id="b5fcb-145">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b5fcb-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="b5fcb-146">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b5fcb-146">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="b5fcb-147">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b5fcb-147">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


