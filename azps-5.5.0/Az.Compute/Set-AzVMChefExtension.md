---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 2821e9404fe4101415aa04a8b0d331b3066563df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144707"
---
# <span data-ttu-id="e2ae7-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="e2ae7-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="e2ae7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ae7-103">Bővítmény hozzáadása virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="e2ae7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e2ae7-104">SYNTAX</span></span>

### <span data-ttu-id="e2ae7-105">Linux</span><span class="sxs-lookup"><span data-stu-id="e2ae7-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2ae7-106">Windows</span><span class="sxs-lookup"><span data-stu-id="e2ae7-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2ae7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e2ae7-107">DESCRIPTION</span></span>
<span data-ttu-id="e2ae7-108">A **Set-AzVMChefExtension** parancsmag hozzáadja a Extension bővítményt a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="e2ae7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e2ae7-109">EXAMPLES</span></span>

### <span data-ttu-id="e2ae7-110">1. példa: Bővítmény hozzáadása windowsos virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="e2ae7-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="e2ae7-111">Ez a parancs hozzáad egy Bővítmény bővítményt egy WindowsVM001 nevű windowsos virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="e2ae7-112">Amikor elindul a virtuális gép, a Modul elindítja a virtuális gépet az Apacs futtatásához.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="e2ae7-113">2. példa: Bővítmény hozzáadása Linux virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="e2ae7-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="e2ae7-114">Ez a parancs hozzáad egy Bővítmény bővítményt egy LinuxVM001 nevű Linux virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="e2ae7-115">Amikor elindul a virtuális gép, a Modul elindítja a virtuális gépet az Apacs futtatásához.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="e2ae7-116">3. példa: Bővítmény hozzáadása egy indítási lehetőségeket is elérhető Windows virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="e2ae7-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="e2ae7-117">Ez a parancs hozzáadja a Bővítmény bővítményt egy WindowsVM002 nevű windowsos virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="e2ae7-118">Amikor elindul a virtuális gép, a Modul elindítja a virtuális gépet az Apacs futtatásához.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="e2ae7-119">A rendszerindítás után a virtuális gép a JSON formátumban megadott BootstrapOptionsra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="e2ae7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2ae7-120">PARAMETERS</span></span>

### <span data-ttu-id="e2ae7-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e2ae7-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae7-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="e2ae7-122">-BootstrapOptions</span></span>
<span data-ttu-id="e2ae7-123">Konfigurációs beállításokat ad meg a client_rb beállításban.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="e2ae7-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="e2ae7-124">-BootstrapVersion</span></span>
<span data-ttu-id="e2ae7-125">A rendszerindítási pont konfigurációjának verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="e2ae7-126">-AbDemonInterval</span><span class="sxs-lookup"><span data-stu-id="e2ae7-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="e2ae7-127">Megadja, hogy a rendszer milyen gyakorisággal (percben) fut.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="e2ae7-128">Ha nem szeretné telepíteni a szoftverszolgáltatást az Azure VM-en, akkor ebben a mezőben állítsa be az értéket 0-ként.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae7-129">-ServerUrl</span><span class="sxs-lookup"><span data-stu-id="e2ae7-129">-ChefServerUrl</span></span>
<span data-ttu-id="e2ae7-130">Url-címként megadja a Kiszolgálón a Kiszolgálón található hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="e2ae7-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="e2ae7-131">-ClientRb</span></span>
<span data-ttu-id="e2ae7-132">A Rb ügyfélprogram teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="e2ae7-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="e2ae7-133">-Daemon</span></span>
<span data-ttu-id="e2ae7-134">A felügyelet nélküli végrehajtáshoz konfigurálja a házirend-ügyfélszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="e2ae7-135">A csomópontplatformnak Windowsnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-135">The node platform should be Windows.</span></span>
<span data-ttu-id="e2ae7-136">Engedélyezett beállítások: "nincs", "szolgáltatás" és "feladat".</span><span class="sxs-lookup"><span data-stu-id="e2ae7-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="e2ae7-137">none – Jelenleg nem lehet szolgáltatásként konfigurálni a házirend-ügyfélszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="e2ae7-138">szolgáltatás – Úgy konfigurálja a házirend-ügyfélprogramot, hogy szolgáltatásként automatikusan a háttérben fusson.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="e2ae7-139">task – Úgy konfigurálja a házirend-ügyfélprogramot, hogy ütemezett feladatként automatikusan fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae7-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ae7-140">-DefaultProfile</span></span>
<span data-ttu-id="e2ae7-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2ae7-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="e2ae7-142">-JsonAttribute</span></span>
<span data-ttu-id="e2ae7-143">Egy JSON-karakterlánc, amely hozzáadódik az első futtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="e2ae7-144">például -JsonAttribute '{"foo" : "bar"}'</span><span class="sxs-lookup"><span data-stu-id="e2ae7-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="e2ae7-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="e2ae7-145">-Linux</span></span>
<span data-ttu-id="e2ae7-146">Azt jelzi, hogy ez a parancsmag virtuális Windows-gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae7-147">-Location</span><span class="sxs-lookup"><span data-stu-id="e2ae7-147">-Location</span></span>
<span data-ttu-id="e2ae7-148">A virtuális gép helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae7-149">-Name</span><span class="sxs-lookup"><span data-stu-id="e2ae7-149">-Name</span></span>
<span data-ttu-id="e2ae7-150">A Bővítmény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae7-151">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e2ae7-151">-NoWait</span></span>
<span data-ttu-id="e2ae7-152">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e2ae7-153">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e2ae7-154">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="e2ae7-154">-OrganizationName</span></span>
<span data-ttu-id="e2ae7-155">A Bővítmény bővítmény szervezeti nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-155">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="e2ae7-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ae7-156">-ResourceGroupName</span></span>
<span data-ttu-id="e2ae7-157">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="e2ae7-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="e2ae7-158">-RunList</span></span>
<span data-ttu-id="e2ae7-159">A Csomópont futtatás listájának megadása.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-159">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="e2ae7-160">-Secret</span><span class="sxs-lookup"><span data-stu-id="e2ae7-160">-Secret</span></span>
<span data-ttu-id="e2ae7-161">Az adattáska értékeinek titkosításához és visszafejtéséhez használt titkosítási kulcs.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="e2ae7-162">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="e2ae7-162">-SecretFile</span></span>
<span data-ttu-id="e2ae7-163">Az adattáska értékeinek titkosításához és visszafejtéséhez használt titkosítási kulcsot tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="e2ae7-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e2ae7-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="e2ae7-165">A virtuális géphez használni használt bővítmény verziója.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-165">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae7-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="e2ae7-166">-ValidationClientName</span></span>
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

### <span data-ttu-id="e2ae7-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="e2ae7-167">-ValidationPem</span></span>
<span data-ttu-id="e2ae7-168">ATerjesztés-érvényesítő .pem fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-168">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="e2ae7-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="e2ae7-169">-VMName</span></span>
<span data-ttu-id="e2ae7-170">Egy virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="e2ae7-171">Ez a parancsmag hozzáadja a Bővítmény bővítményt a paraméter által megadott virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae7-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="e2ae7-172">-Windows</span></span>
<span data-ttu-id="e2ae7-173">Azt jelzi, hogy ez a parancsmag virtuális Windows-gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae7-174">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2ae7-174">-Confirm</span></span>
<span data-ttu-id="e2ae7-175">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae7-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2ae7-176">-WhatIf</span></span>
<span data-ttu-id="e2ae7-177">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2ae7-178">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-178">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae7-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ae7-179">CommonParameters</span></span>
<span data-ttu-id="e2ae7-180">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ae7-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ae7-181">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2ae7-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ae7-182">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2ae7-182">INPUTS</span></span>

### <span data-ttu-id="e2ae7-183">System.String</span><span class="sxs-lookup"><span data-stu-id="e2ae7-183">System.String</span></span>

### <span data-ttu-id="e2ae7-184">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e2ae7-184">System.Boolean</span></span>

## <span data-ttu-id="e2ae7-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2ae7-185">OUTPUTS</span></span>

### <span data-ttu-id="e2ae7-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e2ae7-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e2ae7-187">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e2ae7-187">NOTES</span></span>

## <span data-ttu-id="e2ae7-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2ae7-188">RELATED LINKS</span></span>

[<span data-ttu-id="e2ae7-189">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="e2ae7-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="e2ae7-190">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="e2ae7-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
