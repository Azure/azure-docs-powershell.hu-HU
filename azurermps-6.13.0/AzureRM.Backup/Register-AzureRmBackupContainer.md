---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/register-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: 3431650296c29f06131f946910d1cbc3dc6e6bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672322"
---
# <span data-ttu-id="a9469-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a9469-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="a9469-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9469-102">SYNOPSIS</span></span>
<span data-ttu-id="a9469-103">A tároló rögzítése a biztonsági mentést tartalmazó boltozattal.</span><span class="sxs-lookup"><span data-stu-id="a9469-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9469-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9469-104">SYNTAX</span></span>

### <span data-ttu-id="a9469-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="a9469-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9469-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="a9469-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9469-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9469-107">DESCRIPTION</span></span>
<span data-ttu-id="a9469-108">A **Register-AzureRmBackupContainer** parancsmag a tárolót egy Azure Backup Vault-tárolóval regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="a9469-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="a9469-109">Ha az Azure Backup segítségével szeretné konfigurálni a biztonsági mentést, először regisztrálja a kiszolgálót vagy a virtuális gépet egy biztonsági másolattal.</span><span class="sxs-lookup"><span data-stu-id="a9469-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="a9469-110">Ez a parancsmag egy infrastruktúrát (IaaS) virtuális gépet regisztrál a megadott boltozattal.</span><span class="sxs-lookup"><span data-stu-id="a9469-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="a9469-111">A Register művelet az Azure Virtual machinet a biztonsági mentés boltozatával társítja, és a virtuális gépet a biztonsági életcikluson keresztül követi nyomon.</span><span class="sxs-lookup"><span data-stu-id="a9469-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="a9469-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a9469-112">EXAMPLES</span></span>

### <span data-ttu-id="a9469-113">1. példa: virtuális gép rögzítése biztonsági tárolóban</span><span class="sxs-lookup"><span data-stu-id="a9469-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="a9469-114">Az első parancs a Vault03 nevű boltozatot az Get-AzureRmBackupVault parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a9469-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="a9469-115">A parancs a $Vault változóban tárolja a boltozatot.</span><span class="sxs-lookup"><span data-stu-id="a9469-115">The command stores the vault in the $Vault variable.</span></span>
<span data-ttu-id="a9469-116">A második parancs a Contoso03Vm nevű virtuális gépet $Vault-ban a boltozattal regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="a9469-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="a9469-117">Ez a virtuális gép a ContosoService27 nevű szolgáltatáshoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="a9469-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="a9469-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9469-118">PARAMETERS</span></span>

### <span data-ttu-id="a9469-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9469-119">-DefaultProfile</span></span>
<span data-ttu-id="a9469-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a9469-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9469-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9469-121">-Name</span></span>
<span data-ttu-id="a9469-122">Annak a virtuális gépnek a nevét adja meg, amelyre a parancsmag van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="a9469-122">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9469-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9469-123">-ResourceGroupName</span></span>
<span data-ttu-id="a9469-124">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9469-124">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: V2VM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9469-125">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="a9469-125">-ServiceName</span></span>
<span data-ttu-id="a9469-126">Annak a virtuális gépnek a szolgáltatásának a nevét adja meg, amelyre a parancsmag van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="a9469-126">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>
<span data-ttu-id="a9469-127">A Felhőbeli szolgáltatások nevének általában egy utótag. cloudapp.net kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a9469-127">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="a9469-128">A paraméter megadásakor ne szerepeljen az utótag.</span><span class="sxs-lookup"><span data-stu-id="a9469-128">Do not include the suffix when you specify this parameter.</span></span>
<span data-ttu-id="a9469-129">Ha információt szeretne kapni egy virtuális gépre vonatkozóan, használja az Get-AzureRMVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a9469-129">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="a9469-130">A szolgáltatás neve a Virtual Machine objektum **DeploymentName** tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="a9469-130">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

```yaml
Type: System.String
Parameter Sets: V1VM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9469-131">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="a9469-131">-Vault</span></span>
<span data-ttu-id="a9469-132">Annak a biztonságimásolat-tárolónak a megadása, amelyhez ez a parancsmag a virtuális gépet regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="a9469-132">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="a9469-133">**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a9469-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9469-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9469-134">CommonParameters</span></span>
<span data-ttu-id="a9469-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9469-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9469-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9469-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9469-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9469-137">INPUTS</span></span>

### <span data-ttu-id="a9469-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a9469-138">System.String</span></span>

### <span data-ttu-id="a9469-139">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="a9469-139">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="a9469-140">Paraméterek: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a9469-140">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="a9469-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9469-141">OUTPUTS</span></span>

### <span data-ttu-id="a9469-142">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="a9469-142">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="a9469-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9469-143">NOTES</span></span>

## <span data-ttu-id="a9469-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9469-144">RELATED LINKS</span></span>

[<span data-ttu-id="a9469-145">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="a9469-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


