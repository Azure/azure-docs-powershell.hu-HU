---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: fe1e1075e14e3752024edff1b68db88419d5bcd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497928"
---
# <span data-ttu-id="e6f55-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e6f55-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="e6f55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6f55-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f55-103">A tároló rögzítése a biztonsági mentést tartalmazó boltozattal.</span><span class="sxs-lookup"><span data-stu-id="e6f55-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6f55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6f55-104">SYNTAX</span></span>

### <span data-ttu-id="e6f55-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="e6f55-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6f55-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="e6f55-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6f55-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6f55-107">DESCRIPTION</span></span>
<span data-ttu-id="e6f55-108">A **Register-AzureRmBackupContainer** parancsmag a tárolót egy Azure Backup Vault-tárolóval regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="e6f55-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="e6f55-109">Ha az Azure Backup segítségével szeretné konfigurálni a biztonsági mentést, először regisztrálja a kiszolgálót vagy a virtuális gépet egy biztonsági másolattal.</span><span class="sxs-lookup"><span data-stu-id="e6f55-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="e6f55-110">Ez a parancsmag egy infrastruktúrát (IaaS) virtuális gépet regisztrál a megadott boltozattal.</span><span class="sxs-lookup"><span data-stu-id="e6f55-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="e6f55-111">A Register művelet az Azure Virtual machinet a biztonsági mentés boltozatával társítja, és a virtuális gépet a biztonsági életcikluson keresztül követi nyomon.</span><span class="sxs-lookup"><span data-stu-id="e6f55-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="e6f55-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e6f55-112">EXAMPLES</span></span>

### <span data-ttu-id="e6f55-113">1. példa: virtuális gép rögzítése biztonsági tárolóban</span><span class="sxs-lookup"><span data-stu-id="e6f55-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="e6f55-114">Az első parancs a Vault03 nevű boltozatot az Get-AzureRmBackupVault parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e6f55-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="e6f55-115">A parancs a $Vault változóban tárolja a boltozatot.</span><span class="sxs-lookup"><span data-stu-id="e6f55-115">The command stores the vault in the $Vault variable.</span></span>

<span data-ttu-id="e6f55-116">A második parancs a Contoso03Vm nevű virtuális gépet $Vault-ban a boltozattal regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="e6f55-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="e6f55-117">Ez a virtuális gép a ContosoService27 nevű szolgáltatáshoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="e6f55-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="e6f55-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6f55-118">PARAMETERS</span></span>

### <span data-ttu-id="e6f55-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6f55-119">-Name</span></span>
<span data-ttu-id="e6f55-120">Annak a virtuális gépnek a nevét adja meg, amelyre a parancsmag van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="e6f55-120">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

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

### <span data-ttu-id="e6f55-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f55-121">-ResourceGroupName</span></span>
<span data-ttu-id="e6f55-122">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6f55-122">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="e6f55-123">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="e6f55-123">-ServiceName</span></span>
<span data-ttu-id="e6f55-124">Annak a virtuális gépnek a szolgáltatásának a nevét adja meg, amelyre a parancsmag van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="e6f55-124">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>

<span data-ttu-id="e6f55-125">A Felhőbeli szolgáltatások nevének általában egy utótag. cloudapp.net kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e6f55-125">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="e6f55-126">A paraméter megadásakor ne szerepeljen az utótag.</span><span class="sxs-lookup"><span data-stu-id="e6f55-126">Do not include the suffix when you specify this parameter.</span></span>

<span data-ttu-id="e6f55-127">Ha információt szeretne kapni egy virtuális gépre vonatkozóan, használja az Get-AzureRMVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e6f55-127">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="e6f55-128">A szolgáltatás neve a Virtual Machine objektum **DeploymentName** tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="e6f55-128">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

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

### <span data-ttu-id="e6f55-129">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="e6f55-129">-Vault</span></span>
<span data-ttu-id="e6f55-130">Annak a biztonságimásolat-tárolónak a megadása, amelyhez ez a parancsmag a virtuális gépet regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="e6f55-130">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="e6f55-131">**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e6f55-131">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="e6f55-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f55-132">-DefaultProfile</span></span>
<span data-ttu-id="e6f55-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6f55-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6f55-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f55-134">CommonParameters</span></span>
<span data-ttu-id="e6f55-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6f55-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f55-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f55-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f55-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6f55-137">INPUTS</span></span>

### <span data-ttu-id="e6f55-138">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e6f55-138">AzureRmBackupVault</span></span>

## <span data-ttu-id="e6f55-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6f55-139">OUTPUTS</span></span>

### <span data-ttu-id="e6f55-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="e6f55-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="e6f55-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6f55-141">NOTES</span></span>

## <span data-ttu-id="e6f55-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6f55-142">RELATED LINKS</span></span>

[<span data-ttu-id="e6f55-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e6f55-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


